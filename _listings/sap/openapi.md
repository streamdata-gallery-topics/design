swagger: "2.0"
x-collection-name: SAP
x-complete: 1
info:
  title: SAP Translation Hub
  description: to-provide-users-of-software-in-a-global-market-with-texts-in-their-own-language-translations-are-required--sap-translation-hub-enables-you-to-draw-on-saps-translation-experience-across-multiple-products-and-languages-to-propose-translations-for-short-texts-
  contact:
    name: SAP Translation Hub team
    email: translationhub@sap.com
  version: 1.0.0
host: sandbox.api.sap.com
basePath: /translationhub/api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /collaborationRooms/{collaborationRoomId}/documents/{fileId}/conversion:
    get:
      summary: Gets conversion info of a design file
      description: "Retrieves the information of the conversion event for a design
        file.\nA conversion event converts a design file into a VDS file.  \nSee a
        full list of supported formats in the [online help](https://help.sap.com/viewer/dmc-mn-app-help-customer/710ee60457ca457cbda854c363bcf71f.html)."
      operationId: retrieves-the-information-of-the-conversion-event-for-a-design-filea-conversion-event-converts-a-des
      x-api-path-slug: collaborationroomscollaborationroomiddocumentsfileidconversion-get
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      - in: path
        name: fileId
        description: The ID of a file
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Conversion
      - Info
      - Of
      - Design
      - File
    post:
      summary: Converts a design file
      description: |-
        Invokes a conversion event that converts a design file into a VDS file.

        See a full list of supported formats in the [online help](https://help.sap.com/viewer/dmc-mn-app-help-customer/710ee60457ca457cbda854c363bcf71f.html).
      operationId: invokes-a-conversion-event-that-converts-a-design-file-into-a-vds-filesee-a-full-list-of-supported-f
      x-api-path-slug: collaborationroomscollaborationroomiddocumentsfileidconversion-post
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      - in: path
        name: fileId
        description: The ID of a file
      - in: header
        name: Prefer
        description: Sets the conversion event to run asynchronously
      responses:
        200:
          description: Successful response
      tags:
      - Converts
      - Design
      - File
  /collaborationRooms/{collaborationRoomId}/thumbnails:
    get:
      summary: Retrieves the thumbnail of a design file
      description: |-
        Retrieves the thumbnail information in a collaboration room.
        Each design file has a corresponding thumbnail file automatically generated.
      operationId: retrieves-the-thumbnail-information-in-a-collaboration-roomeach-design-file-has-a-corresponding-thum
      x-api-path-slug: collaborationroomscollaborationroomidthumbnails-get
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - Thumbnail
      - Of
      - Design
      - File
  /documents/collaborationRooms/{collaborationRoomId}/thumbnail/download:
    get:
      summary: Downloads the thumbnail of a design file
      description: Downloads the thumbnail selected as the icon for a collaboration
        room.
      operationId: downloads-the-thumbnail-selected-as-the-icon-for-a-collaboration-room
      x-api-path-slug: documentscollaborationroomscollaborationroomidthumbnaildownload-get
      parameters:
      - in: path
        name: collaborationRoomId
        description: The ID of a collaboration room
      responses:
        200:
          description: Successful response
      tags:
      - Downloads
      - Thumbnail
      - Of
      - Design
      - File
  /partsAnalysis/worklists/{worklistId}/parts/{partId}/designFiles/{designFileId}:
    get:
      summary: Downloads the design file of a part
      description: Downloads the design file for a part
      operationId: downloads-the-design-file-for-a-part
      x-api-path-slug: partsanalysisworklistsworklistidpartspartiddesignfilesdesignfileid-get
      parameters:
      - in: path
        name: designFileId
        description: A self-generated ID for a design file
      - in: path
        name: partId
        description: A self-generated ID for a part in the worklist
      - in: path
        name: worklistId
        description: The UUID for a published worklist
      responses:
        200:
          description: Successful response
      tags:
      - Downloads
      - Design
      - File
      - Of
      - Part
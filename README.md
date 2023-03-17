# swagger
info: 
  contact: {}
  version: '0.0.1'
  description: students info
  title: student
paths:
  /student/{student_id}:
    get:
      consumes:
        - application/json
      description: string by id
      parameters:
        - description: students id
          in: path
          name: student_id
          required: true
          type: integer
      produces:
        - application/json
      responses:
        "200":
          description: ok
          schema: 
            type: string
        "400":
          description: required id
          schema:
            type: string
        "404":
          description: server id not found
          schema:
            type: string
        "500":
          description: error id
          schema: 
            type: string
     
     
      get:
        consumes:
          - application/json
        parameters:
          - description: students id
            in: path
            required: true
            type: integer
        produces:
          - application/json
        responses:
          "200":
            description: ok
            schema: 
              type: string
          "400":
            description: required id
            schema:
              type: string
          "404":
            description: server id not found
            schema:
              type: string
          "500":
            description: error id
            schema: 
              type: string
schemes:
- http
- https
securityDefinitions: 
  BasicAuth:
   type: basic
swagger: "2.0"
   
definitions:
  student_view:
    title: student view
    description: student view
    type: object
    properties:
      id:
        type: number
      name:
        type: string

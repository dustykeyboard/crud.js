# crud.js
Simple JavaScript library to manage JSON objects via CRUD api

## Usage

    var crud = new Crud('https://path.to.api/', 'EXAMPLE-AUTH-TOKEN');
    
    var object = {
      'title': 'Original Object'
    };
  
    crud.create(
      'objects',
      object,
      function(json){console.log(json);},
      function(){console.error('failed to create');
    );
    
    crud.read(
      'objects',
      function(json){console.log(json);},
      function(){console.error('failed to read');
    );
    
    object.title = 'Updated Object';
    cred.update(
      'objects/1',
      object,
      function(json){console.log(json);},
      function(){console.error('failed to read');
    );
    
    cred.delete(
      'objects/1',
      function(json){console.log(json);},
      function(){console.error('failed to delete');
    );

## Example

A full example can be found in the [apitest](https://github.com/dustykeyboard/apitest) repo.

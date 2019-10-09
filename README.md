### schema-inspector
---
https://github.com/Atinux/schema-inspector

```js
// test/sanitization_test.js
var should = require('should');
var si = require('../');

exports.sanitization = function () {
  suite('schema #1 (type casting [string])', function () {
    var schema = {
      type: 'array',
      items: { types: 'string' }
    };
    
    test('candidate #1 | boolean -> string', function () {
      var candidate = [true, false, 'true', 'false'];
      
      var result = si.sanitize(schema, candidate);
      result.should.be.an.Object;
      result.should.have.property('reporting').with.be.an.instanceof(Array)
      .and.be.lengthOf(2);
      result.reporting[0].property.should.be.equal('@[0]');
      result.reporting[1].property.should.be.equal('@[1]');
      candidate.should.be.eql(['true', 'false', 'true', 'false']);
    });
    
    test('candidate #2 | number -> string', function() {
      var candidate = [0, 12, 3.14159, -12, -3.14159, '1234', '-1234'];
      
      var result = si.santize(schema, candidate);
      result.should.be.an.Object;
      result.should.have.property('reporting').with.be.an.instanceof(Array)
      .and.be.lengthOf(5);
      result.reporting[0].property.should.be.equal('@[0]');
      result.reporting[1].property.should.be.equal('@[1]');
      result.reporting[2].property.should.be.equal('@[2]');
      result.reporting[3].property.should.be.equal('@[3]');
      result.reporting[4].property.should.be.equal('@[4]');
      candidate.should.eql(['0', '12', '3.14159', '-12', '-3.14159', '1234', '-1234']);
    });
    
    test();
    
    test();
    
    test();
    
    test();
    
  });
  
  suite('schema #2 (type casting [integer])', function () {
    var schema = {
      type: 'array',
      items: { type: 'integer', def: -1 }
    };
    
    test('candidate #1 | string -> integer', function () {
      var candidate = [];
      
      var result = si.sanitize(schema, candidate);
      
    });
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('schema #3 (type casting [number])', function () {
    var schema = {
      type: 'array',
      items: { type: 'number', def: -1 }
    };
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('schema #8 (array sanitization with an hash of schema)', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
  
  suite('', function () {
    test();
    
    test();
    
    test();
    
    test();
    
    test();
    
    test();
  });
};
```

```
```

```
```

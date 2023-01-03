# Mongo-I
nomard Youtube Code Challenge 7

```
(1) import mongoose from "mongoose": mongoose를 불러옵니다.

(2) const MovieSchema = mongoose.Schema()
    Movie 모델이 될 schema(형태)를 정의합니다. 스키마는 MongoDB 컬렉션에 매핑되며 해당 컬렉션 내의 문서 모양을 정의합니다.

(3) { title: { type: String, required: true }, summary: { type: String, required: true }, … }
    type: String, type: Number
    각각의 key별로 알맞은 데이터 타입을 정의해줍니다. 모델 작업 시 데이터 타입을 정의해 두면, 올바르지 않은 데이터를 입력하는
    실수를 범하더라도 몽구스가 잘못 입력된 데이터를 도큐먼트에 기록하지 않습니다.
    required: true
    각 key에 required: true라고 입력하면 각 필드는 반드시 입력해야 하는 필드가 됩니다. 그러면 사용자가 필드 중 하나를 작성하지
    못하는 실수를 하더라도 몽구스가 오류를 잡아줄 수 있습니다. 데이터의 내용이 구체적일수록 유효성 검증이 더 효과적으로 수행됩니다.
    genres: [{ type: String, required: true }]
    genres는 String의 배열로 작성해야 하기 때문에 위의 코드처럼 작성하면 됩니다.

(4) const Movie = mongoose.model("Movie", MovieSchema)
    mongoose.model("모델이 사용하는 컬렉션의 단수(singular) 이름", 스키마 이름)을 사용하여 MovieSchema를 Movie 모델로 컴파일합니다.

(5) export default Movie: Movie를 export default로 내보냅니다.

(6) import "./models/Movie": index.js에서 Movie 모델을 불러옵니다.
```

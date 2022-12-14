**DİKKAT! Axios v.1.2.1 ile kullanıldığında hata veriyor. Hata alıyorsanız v.1.1.3 ile hatayı giderebilirsiniz.**

-  Bu fonksiyon **"async"** olarak tanımlanmalı ve default olarak dışa aktarılmalıdır. Fonksiyonun içindeki asenkron fonksiyonlar **"await"** ile tanımlanmalıdır.
-  Fonksiyon **Number** tipinde tek parametre alır. Bu parametre **user id**'yi belirtir.
-  Fonksiyonun görevi aşağıdaki endpoint'e giderek parametrede verilen user id ile ilgili kullanıcının verilerini çekmek olmalı. İstekleri **"axios"** kütüphanesini kullanarak yapmanız gerekiyor. İsteği yaparken aşağıdaki endpointin sonundaki rakamı parametrede gelen user id'ile değiştirmeniz gerekiyor.

	 [https://jsonplaceholder.typicode.com/users/1](https://jsonplaceholder.typicode.com/users/1)

-  Yine aynı fonksiyonun içerisinde ve yine aynı user id için bir de "posts" isteği yapılmalıdır.İsteği yaparken aşağıdaki endpoint'in sonundaki rakamı parametrede gelen user id'ile değiştirmeniz gerekiyor.

	[https://jsonplaceholder.typicode.com/posts?userId=1](https://jsonplaceholder.typicode.com/posts?userId=1)

-  Artık elimizde kullanıcı bilgileri ve bu kullanıcının post'ları var. Bu iki veriyi birleştirip return edin. Birleştirme sonucunda elinizde aşağıdaki gibi bir obje bulunması gerekiyor.

```js
{
  id: 1,
  name: 'Leanne Graham',
  username: 'Bret',
  email: 'Sincere@april.biz',
  address: {
    street: 'Kulas Light',
    suite: 'Apt. 556',
    city: 'Gwenborough',
    zipcode: '92998-3874',
    geo: { lat: '-37.3159', lng: '81.1496' }
  },
  phone: '1-770-736-8031 x56442',
  website: 'hildegard.org',
  company: {
    name: 'Romaguera-Crona',
    catchPhrase: 'Multi-layered client-server neural-net',
    bs: 'harness real-time e-markets'
  }
}
[
  {
    userId: 1,
    id: 1,
    title: 'sunt aut facere repellat provident occaecati excepturi optio reprehenderit',
    body: 'quia et suscipit\n' +
      'suscipit recusandae consequuntur expedita et cum\n' +
      'reprehenderit molestiae ut ut quas totam\n' +
      'nostrum rerum est autem sunt rem eveniet architecto'
  },
  {
    userId: 1,
    id: 2,
    title: 'qui est esse',
    body: 'est rerum tempore vitae\n' +
      'sequi sint nihil reprehenderit dolor beatae ea dolores neque\n' +
      'fugiat blanditiis voluptate porro vel nihil molestiae ut reiciendis\n' +
      'qui aperiam non debitis possimus qui neque nisi nulla'
  },
  {
    userId: 1,
    id: 3,
    title: 'ea molestias quasi exercitationem repellat qui ipsa sit aut',
    body: 'et iusto sed quo iure\n' +
      'voluptatem occaecati omnis eligendi aut ad\n' +
      'voluptatem doloribus vel accusantium quis pariatur\n' +
      'molestiae porro eius odio et labore et velit aut'
  },
  {
    userId: 1,
    id: 4,
    title: 'eum et est occaecati',
    body: 'ullam et saepe reiciendis voluptatem adipisci\n' +
      'sit amet autem assumenda provident rerum culpa\n' +
      'quis hic commodi nesciunt rem tenetur doloremque ipsam iure\n' +
      'quis sunt voluptatem rerum illo velit'
  },
  {
    userId: 1,
    id: 5,
    title: 'nesciunt quas odio',
    body: 'repudiandae veniam quaerat sunt sed\n' +
      'alias aut fugiat sit autem sed est\n' +
      'voluptatem omnis possimus esse voluptatibus quis\n' +
      'est aut tenetur dolor neque'
  },
  {
    userId: 1,
    id: 6,
    title: 'dolorem eum magni eos aperiam quia',
    body: 'ut aspernatur corporis harum nihil quis provident sequi\n' +
      'mollitia nobis aliquid molestiae\n' +
      'perspiciatis et ea nemo ab reprehenderit accusantium quas\n' +
      'voluptate dolores velit et doloremque molestiae'
  },
  {
    userId: 1,
    id: 7,
    title: 'magnam facilis autem',
    body: 'dolore placeat quibusdam ea quo vitae\n' +
      'magni quis enim qui quis quo nemo aut saepe\n' +
      'quidem repellat excepturi ut quia\n' +
      'sunt ut sequi eos ea sed quas'
  },
  {
    userId: 1,
    id: 8,
    title: 'dolorem dolore est ipsam',
    body: 'dignissimos aperiam dolorem qui eum\n' +
      'facilis quibusdam animi sint suscipit qui sint possimus cum\n' +
      'quaerat magni maiores excepturi\n' +
      'ipsam ut commodi dolor voluptatum modi aut vitae'
  },
  {
    userId: 1,
    id: 9,
    title: 'nesciunt iure omnis dolorem tempora et accusantium',
    body: 'consectetur animi nesciunt iure dolore\n' +
      'enim quia ad\n' +
      'veniam autem ut quam aut nobis\n' +
      'et est aut quod aut provident voluptas autem voluptas'
  },
  {
    userId: 1,
    id: 10,
    title: 'optio molestias id quia eum',
    body: 'quo et expedita modi cum officia vel magni\n' +
      'doloribus qui repudiandae\n' +
      'vero nisi sit\n' +
      'quos veniam quod sed accusamus veritatis error'
  }
]
PS C:\Users\msami\Documents\Sites\React_First_Assignment> node app.js
{
  id: 2,
  name: 'Ervin Howell',
  username: 'Antonette',
  email: 'Shanna@melissa.tv',
  address: {
    street: 'Victor Plains',
    suite: 'Suite 879',
    city: 'Wisokyburgh',
    zipcode: '90566-7771',
    geo: { lat: '-43.9509', lng: '-34.4618' }
  },
  phone: '010-692-6593 x09125',
  website: 'anastasia.net',
  company: {
    name: 'Deckow-Crist',
    catchPhrase: 'Proactive didactic contingency',
    bs: 'synergize scalable supply-chains'
  }
} [
  {
    userId: 2,
    id: 11,
    title: 'et ea vero quia laudantium autem',
    body: 'delectus reiciendis molestiae occaecati non minima eveniet qui voluptatibus\n' +
      'accusamus in eum beatae sit\n' +
      'vel qui neque voluptates ut commodi qui incidunt\n' +
      'ut animi commodi'
  },
  {
    userId: 2,
    id: 12,
    title: 'in quibusdam tempore odit est dolorem',
    body: 'itaque id aut magnam\n' +
      'praesentium quia et ea odit et ea voluptas et\n' +
      'sapiente quia nihil amet occaecati quia id voluptatem\n' +
      'incidunt ea est distinctio odio'
  },
  {
    userId: 2,
    id: 13,
    title: 'dolorum ut in voluptas mollitia et saepe quo animi',
    body: 'aut dicta possimus sint mollitia voluptas commodi quo doloremque\n' +
      'iste corrupti reiciendis voluptatem eius rerum\n' +
      'sit cumque quod eligendi laborum minima\n' +
      'perferendis recusandae assumenda consectetur porro architecto ipsum ipsam'
  },
  {
    userId: 2,
    id: 14,
    title: 'voluptatem eligendi optio',
    body: 'fuga et accusamus dolorum perferendis illo voluptas\n' +
      'non doloremque neque facere\n' +
      'ad qui dolorum molestiae beatae\n' +
      'sed aut voluptas totam sit illum'
  },
  {
    userId: 2,
    id: 15,
    title: 'eveniet quod temporibus',
    body: 'reprehenderit quos placeat\n' +
      'velit minima officia dolores impedit repudiandae molestiae nam\n' +
      'voluptas recusandae quis delectus\n' +
      'officiis harum fugiat vitae'
  },
  {
    userId: 2,
    id: 16,
    title: 'sint suscipit perspiciatis velit dolorum rerum ipsa laboriosam odio',
    body: 'suscipit nam nisi quo aperiam aut\n' +
      'asperiores eos fugit maiores voluptatibus quia\n' +
      'voluptatem quis ullam qui in alias quia est\n' +
      'consequatur magni mollitia accusamus ea nisi voluptate dicta'
  },
  {
    userId: 2,
    id: 17,
    title: 'fugit voluptas sed molestias voluptatem provident',
    body: 'eos voluptas et aut odit natus earum\n' +
      'aspernatur fuga molestiae ullam\n' +
      'deserunt ratione qui eos\n' +
      'qui nihil ratione nemo velit ut aut id quo'
  },
  {
    userId: 2,
    id: 18,
    title: 'voluptate et itaque vero tempora molestiae',
    body: 'eveniet quo quis\n' +
      'laborum totam consequatur non dolor\n' +
      'ut et est repudiandae\n' +
      'est voluptatem vel debitis et magnam'
  },
  {
    userId: 2,
    id: 19,
    title: 'adipisci placeat illum aut reiciendis qui',
    body: 'illum quis cupiditate provident sit magnam\n' +
      'ea sed aut omnis\n' +
      'veniam maiores ullam consequatur atque\n' +
      'adipisci quo iste expedita sit quos voluptas'
  },
  {
    userId: 2,
    id: 20,
    title: 'doloribus ad provident suscipit at',
    body: 'qui consequuntur ducimus possimus quisquam amet similique\n' +
      'suscipit porro ipsam amet\n' +
      'eos veritatis officiis exercitationem vel fugit aut necessitatibus totam\n' +
      'omnis rerum consequatur expedita quidem cumque explicabo'
  }
```

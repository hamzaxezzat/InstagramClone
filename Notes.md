Installing Packets ($npm install --)

* date-fns #date
* firebase 
* react-loading-skeleton #
* install-eslint 
$ exec 3<&1;bash <&3 <(curl https://raw.githubusercontent.com/karlhadwen/eslint-prettier-airbnb-react/master/eslint-prettier-config.sh 2> /dev/null)



Need to Study
* md


Note
- Never put your images locally, put in CDN for example
    (How to store Images in react)




// Client side renderd app: react (cra)
    // -> DB Firebase
    // -> react-loadin-skeleton
    // -> tailwind
    
// folder structure
    // src
        // -> components,
        // -> contants,
        // -> context,
        // -> hooks,
        // -> helpers,
        // -> lib (firebase is going to live)
        // -> services (firebase functions)
        // -> style (talwind's folder (app/tailwind))



Firebase
// Development rules
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if
          request.time < timestamp.date(2022, 11, 19);
    }
  }
}


# Github Popular Repos

In this project, I have completed the **Github Popular Repos** application by applying the concepts learned so far.

### Refer to the images below:

![Github Popular Repos Output](https://assets.ccbp.in/frontend/content/react-js/github-popular-repos-output.gif)

**Failure View**

![Github Popular Repos Failure View](https://assets.ccbp.in/frontend/content/react-js/github-popular-repos-error-view-output.gif)

### Design Files

- Extra Small (Size < 576px) and Small (Size >= 576px)
  
  ![Small Design](https://assets.ccbp.in/frontend/content/react-js/github-repos-sm-outputs.png)
  
- Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Success
  
  ![Medium Success Design](https://assets.ccbp.in/frontend/content/react-js/github-repos-lg-success-output.png)
  
- Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Loading
  
  ![Medium Loading Design](https://assets.ccbp.in/frontend/content/react-js/github-repos-lg-loading-output.png)
  
- Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Failure
  
  ![Medium Failure Design](https://assets.ccbp.in/frontend/content/react-js/github-repos-error-view-lg-output.png)

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### Completion Instructions

<details>
<summary>Functionality to be added</summary>
<br/>

The app has the following functionalities:

- When the app is opened initially:

  - An HTTP GET request is made to **githubReposApiUrl** with query parameter as `language` and its initial value as `ALL`
  - **_loader_** is displayed while fetching the data
  - After the data is fetched successfully, the repositories list received in the response is displayed

- When a language filter is active:

  - An HTTP GET request is made to the above-mentioned URL with the `id` of the active language
  - **_loader_** is displayed while fetching the data
  - After the data is fetched successfully, the repositories list received in the response is displayed

- The `GithubPopularRepos` component is provided with `languageFiltersData`. It consists of a list of language filter objects with the following properties in each language filter object:

  |   Key    | Data Type |
  | :------: | :-------: |
  |    id    |  String   |
  | language |  String   |

</details>

<details>

<summary>API Requests & Responses</summary>
<br>

**githubReposApiUrl**

#### API: `https://apis.ccbp.in/popular-repos`

#### Example: `https://apis.ccbp.in/popular-repos?language=ALL`

#### Method: `GET`

#### Description:

Returns a response containing the list of repositories

#### Response

```json
{
  "popular_repos": [
    {
	  "name": "freeCodeCamp",
      "id": 28457823,
      "issues_count": 154,
      "forks_count": 26651,
      "stars_count": 331304,
      "avatar_url": "https://avatars.githubusercontent.com/u/9892522?v=4"
    },
      ...
  ],
}
```

</details>

<details>
<summary>Components Structure</summary>

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/github-popular-repos-component-breakdown-structure.png" alt="component-breakdown-structure" style="max-width:100%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

</details>

<details>
<summary>Implementation Files</summary>
<br/>

The following files were used to complete the implementation:

- `src/components/GithubPopularRepos/index.js`
- `src/components/GithubPopularRepos/index.css`
- `src/components/LanguageFilterItem/index.js`
- `src/components/LanguageFilterItem/index.css`
- `src/components/RepositoryItem/index.js`
- `src/components/RepositoryItem/index.css`
</details>

### Quick Tips

<details close>
<summary>Click to view</summary>
<br>

- To display the animated loader, we need to import the `Loader` component using the below statement:

  ```jsx
  import Loader from 'react-loader-spinner'
  ```

- In order to display the given animated loader, pass the `type` and `color` props to the `Loader` component with values as **ThreeDots** and **#0284c7**, respectively

  ```jsx
  <Loader type="ThreeDots" color="#0284c7" height={80} width={80} />
  ```

    <br/>  
  </details>

### Important Note

<details>
<summary>Click to view</summary>

<br/>

**The following instructions are required for the tests to pass:**

- Wrap the `Loader` component with an HTML container element and add the `data-testid` attribute value as **loader** to it

  ```jsx
  <div data-testid="loader">
    <Loader type="ThreeDots" color="#0284c7" height={80} width={80} />
  </div>
  ```

</details>

### Resources

<details>
<summary>Image URLs</summary>

- [https://assets.ccbp.in/frontend/react-js/stars-count-img.png](https://assets.ccbp.in/frontend/react-js/stars-count-img.png) alt should be **stars**
- [https://assets.ccbp.in/frontend/react-js/forks-count-img.png](https://assets.ccbp.in/frontend/react-js/forks-count-img.png) alt should be **forks**
- [https://assets.ccbp.in/frontend/react-js/issues-count-img.png](https://assets.ccbp.in/frontend/react-js/issues-count-img.png) alt should be **open issues**
- [https://assets.ccbp.in/frontend/react-js/api-failure-view.png](https://assets.ccbp.in/frontend/react-js/api-failure-view.png) alt should be **failure view**

</details>

<details>
<summary>Colors</summary>

<br/>

<div style="background-color: #0284c7; width: 150px; padding: 10px; color: white">Hex: #0284c7</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #0f172a; width: 150px; padding: 10px; color: white">Hex: #0f172a</div>
<div style="background-color: #f8f8ff; width: 150px; padding: 10px; color: black">Hex: #f8f8ff</div>
<div style="background-color: #e73959; width: 150px; padding: 10px; color: white">Hex: #e73959</div>
<div style="background-color: #1e293b; width: 150px; padding: 10px; color: white">Hex: #1e293b</div>

</details>

<details>
<summary>Font-families</summary>

- Roboto
- Lobster

</details>

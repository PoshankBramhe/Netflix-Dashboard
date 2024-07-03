<h1>Netflix Dashboard</h1>
<p>This Tableau dashboard provides a comprehensive analysis of Netflix's movies and TV shows based on various attributes such as release year, rating, duration, genre, and country of origin.</p>


![image](https://github.com/PoshankBramhe/Netflix-Dashboard/assets/154652656/fd2a732d-f95f-493e-a090-36bb09d46e0d)


<h2>Data Source</h2>
<p>The dataset includes information on Netflix titles and consists of the following columns:</p>
<ul>
  <li><strong>show_id</strong>: Unique identifier for each show.</li>
  <li><strong>type</strong>: Indicates whether the title is a movie or TV show.</li>
  <li><strong>title</strong>: Name of the show.</li>
  <li><strong>director</strong>: Director of the show.</li>
  <li><strong>cast</strong>: Main cast members of the show.</li>
  <li><strong>country</strong>: Country where the show was produced.</li>
  <li><strong>date_added</strong>: Date the show was added to Netflix.</li>
  <li><strong>release_year</strong>: Year the show was released.</li>
  <li><strong>rating</strong>: Audience rating of the show.</li>
  <li><strong>duration</strong>: Duration of the show (in minutes for movies and seasons for TV shows).</li>
  <li><strong>listed_in</strong>: Genres or categories the show is listed under.</li>
  <li><strong>description</strong>: Brief description of the show.</li>
</ul>

<h2>ETL Process</h2>
<h3>Extraction</h3>
<p>The data is extracted from a CSV file containing the aforementioned columns.</p>

<h3>Transformation</h3>
<ul>
  <li><strong>Data Cleaning:</strong>
    <ul>
      <li>Remove duplicates to ensure each show is unique.</li>
      <li>Handle missing values:
        <ul>
          <li>Fill missing values for <code>director</code> and <code>cast</code> with 'Unknown'.</li>
          <li>Drop records with missing <code>country</code>, <code>date_added</code>, <code>release_year</code>, <code>rating</code>, <code>duration</code>, and <code>listed_in</code> values.</li>
        </ul>
      </li>
      <li>Standardize the format of the <code>date_added</code> column to ensure consistency.</li>
    </ul>
  </li>
  <li><strong>Data Formatting:</strong>
    <ul>
      <li>Convert <code>release_year</code> and <code>duration</code> columns to integer type.</li>
      <li>Ensure <code>rating</code> column uses consistent rating labels.</li>
    </ul>
  </li>
  <li><strong>Data Enrichment:</strong>
    <ul>
      <li>Extract and create separate columns for genres from the <code>listed_in</code> column.</li>
      <li>Derive additional insights such as the number of titles per year, the number of titles per country, and the distribution of ratings.</li>
    </ul>
  </li>
</ul>

<h3>Loading</h3>
<p>The cleaned and transformed data is then loaded into Tableau for visualization and analysis.</p>

<h2>Dashboard Components</h2>
<p>The dashboard is divided into several sections, each providing different insights into the Netflix catalog.</p>

<h3>1. Header Section</h3>
<ul>
  <li><strong>Release Year:</strong> Displays the year of release for the selected title.</li>
  <li><strong>Rating:</strong> Displays the audience rating for the selected title.</li>
  <li><strong>Duration:</strong> Shows the duration of the selected title in minutes.</li>
  <li><strong>Listed In:</strong> Categories or genres the selected title is listed under.</li>
  <li><strong>Description:</strong> Brief summary of the selected title's plot or theme.</li>
</ul>

<h3>2. Movies & TV Shows by Country</h3>
<p>This world map visualization shows the distribution of Netflix titles by country. The color intensity represents the number of titles produced in each country. Hovering over a country provides the exact count of titles from that country.</p>

<h3>3. Rating Distribution</h3>
<p>A bar chart showing the distribution of titles by their audience ratings. This chart helps in understanding the variety of content ratings available on Netflix, from G to TV-MA.</p>

<h3>4. Distribution of Movies vs. TV Shows</h3>
<p>A pie chart showing the proportion of movies to TV shows in the Netflix catalog. This chart provides a quick overview of the type of content available.</p>

<h3>5. Top 10 Genres</h3>
<p>A horizontal bar chart listing the top 10 genres/categories with the highest number of titles. This helps in identifying the most popular types of content on Netflix.</p>

<h3>6. Movies & TV Shows by Years</h3>
<p>An area chart displaying the number of movies and TV shows released over the years. This section helps in understanding the trends in content production and release on Netflix over time.</p>

<h2>Interaction and Filters</h2>
<ul>
  <li><strong>Title Dropdown:</strong> Allows users to select a specific title to view detailed information in the header section.</li>
  <li><strong>Type Filter:</strong> Users can filter the dashboard to display only movies, only TV shows, or all titles.</li>
</ul>

<h2>Usage Instructions</h2>
<ol>
  <li><strong>Interacting with the Map:</strong> Hover over countries to see the count of titles from each country.</li>
  <li><strong>Filtering by Title:</strong> Use the dropdown menu to select a specific title and view detailed information in the header section.</li>
  <li><strong>Filtering by Type:</strong> Use the type filter to switch between movies, TV shows, or view all content.</li>
  <li><strong>Exploring Genres:</strong> View the top 10 genres to understand popular content categories.</li>
  <li><strong>Analyzing Trends:</strong> Use the area chart to explore how the release of movies and TV shows has changed over the years.</li>
</ol>

<h2>Conclusion</h2>
<p>This dashboard provides a comprehensive overview of Netflix's content library, allowing users to explore and analyze various aspects of the available titles. The visualizations help in understanding the distribution of content by country, rating, genre, and release year, providing valuable insights into Netflix's offerings.</p>

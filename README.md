# Netflix-Genre-Explorer
Analyze Netflix viewing trends across countries and time to understand content preferences and predict popular genres.

Key Features:

Collected Netflix data from public datasets (e.g., Kaggle, IMDb).

Cleaned and transformed data using Pandas & NumPy.

Built insightful visualizations with Matplotlib/Seaborn/Power BI:

Genre heatmaps by country

Release year vs. viewer rating analysis

Performed trend analysis on content types (TV shows vs. movies).

Created an interactive dashboard to explore popular genres by region and time.

Tools Used:
Python, Pandas, NumPy, Matplotlib/Seaborn, Power BI or Tableau


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Netflix Genre Explorer</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <style>
        body {
            background-color: #f0f0f0;
        }
        .genre-card {
            width: 100%;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .genre-card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
        }
        .genre-card h5, .genre-card button {
            padding: 10px;
        }
        .modal-dialog {
            max-width: 800px;
        }
        .modal-content {
            background-color: #f0f0f0;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <a class="navbar-brand" href="#">Netflix Genre Explorer</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item active">
                    <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">About</a>
                </li>
            </ul>
            <form class="form-inline my-2 my-lg-0">
                <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
                <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
            </form>
        </div>
    </nav>

    <div class="container mt-5">
        <h2>Genres</h2>
        <div class="row">
            <!-- Genre Cards -->
            <div class="col-md-3" *ngFor="let genre of genres">
                <div class="genre-card">
                    <img src="https://picsum.photos/200/300" alt="Genre Image">
                    <h5>{{ genre.name }}</h5>
                    <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#{{ genre.id }}Modal">View</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Example Modal Template -->
    <div class="modal fade" id="actionModal" tabindex="-1" role="dialog" aria-labelledby="actionModalLabel" aria-hidden="true">
        <div class="modal-dialog" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="actionModalLabel">Action Movies</h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    <ul>
                        <li>Movie 1</li>
                        <li>Movie 2</li>
                        <li>Movie 3</li>
                    </ul>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js"></script>
</body>
</html>

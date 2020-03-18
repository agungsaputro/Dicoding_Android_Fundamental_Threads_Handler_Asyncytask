# Dicoding_Android_Fundamental_Threads_Handler_Asyncytask
Latihan 4 : MyAnsyntask

Android AsyncTask: You can interact with UI thread (Main Thread) with AsynTask when you have to do some background task. AsyncTask class perform background operations and publish results on the UI thread without having to manipulate threads.
AysnTask performs an operation (or any task) in the background and publishes results in UI Thread. An asynchronous task is defined by 3 generic types, called,ParamsProgress and Result.
    Params,  the parameters sent to the task upon execution.

    Progress, the progress units published during the background computation.

    Result, the result of the background computation.
    
There are 4 methods in Async task: onPreExecute, doInBackground, onProgressUpdate and onPostExecute.

    onPreExecute(), invoked on the UI thread before the task is executed.

    doInBackground(Params...), invoked on the background thread immediately after onPreExecute() finishes executing.

    onProgressUpdate(Progress...), invoked on the UI thread after a call to publishProgress(Progress...).

    onPostExecute(Result), invoked on the UI thread after the background computation finishes.
    
Rules of Using AsyncTask

    First rule AsyncTask class must be loaded on the UI thread, it will be done automatically.

    execute(Params...) must be invoked on the UI thread.

    Do not call onPreExecute(), onPostExecute(Result), doInBackground(Params...), onProgressUpdate(Progress...) manually.

    The task can be executed only once (an exception will be thrown if a second execution is attempted.)

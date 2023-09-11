# Steps to setup

- pip install sklearn
- pip install -r requirements.txt
- Create Digital_Voting Database in PostgreSQL.
- Configure Database section in settings.py.
- python manage.py migrate
- Create an account on https://2factor.in and paste api key from your 2factor account in voter/views.py at line 33, 48, 288 and 308 for SMS OTP verification.
- Update email_id and password in settings.py for email OTP verification.
- python manage.py createsuperuser
- python manage.py runserver
- Login to Django Administration page (http://127.0.0.1:8000/admin) and add details of superuser in EC_Admins.
- Navigate to http://127.0.0.1:8000 and Login as admin, add voter and add candidate details and logout.
- Click on Register and fill voter registration form, record and upload video of 5-10 seconds for face recognition.

<!-- pip install scikit-learn -->
<!-- python -m venv myenv
source myenv/bin/activate  # On Windows, use `myenv\Scripts\activate` -->

       <!-- function DOB() {
            var lblError = document.getElementById("lblError");

            //Get the date from the TextBox.
            var dateString = document.getElementById("dob").value;
            var regex = /(((0|1)[0-9]|2[0-9]|3[0-1])\/(0[1-9]|1[0-2])\/((19|20)\d\d))$/;

            //Check whether valid dd/MM/yyyy Date Format.
            if (regex.test(dateString)) {
                var parts = dateString.split("/");
                var dtDOB = new Date(parts[1] + "/" + parts[0] + "/" + parts[2]);
                var dtCurrent = new Date();
                lblError.innerHTML = "Eligibility 18 years ONLY."
                if (dtCurrent.getFullYear() - dtDOB.getFullYear() < 18) {
                    return false;
                }

                if (dtCurrent.getFullYear() - dtDOB.getFullYear() == 18) {

                    //CD: 11/06/2018 and DB: 15/07/2000. Will turned 18 on 15/07/2018.
                    if (dtCurrent.getMonth() < dtDOB.getMonth()) {
                        return false;
                    }
                    if (dtCurrent.getMonth() == dtDOB.getMonth()) {
                        //CD: 11/06/2018 and DB: 15/06/2000. Will turned 18 on 15/06/2018.
                        if (dtCurrent.getDate() < dtDOB.getDate()) {
                            return false;
                        }
                    }
                }
                lblError.innerHTML = "";
                return true;
            } else {
                lblError.innerHTML = "Enter date in dd/MM/yyyy format ONLY."
                return false;
            }
        } -->

Fix to Tanggal Bulan Tahun

 public void setTanggal(View v) { final Calendar
            c = Calendar.getInstance(); int thn =
            c.get(Calendar.YEAR); int bln =
            c.get(Calendar.MONTH); int tgl =
            c.get(Calendar.DAY_OF_MONTH);
        DatePickerDialog datePickerDialog = new DatePickerDialog(MainActivity.this, new
                DatePickerDialog.OnDateSetListener() {
                    @Override
                    public void onDateSet(DatePicker view, int thn, int bln, int tgl) {
                        tanggal.setText(tgl + "-" + (bln+ 1) + "-" + thn);
                    }
                }, tgl, bln, thn); datePickerDialog.show();
    }

# react-native-china-city-picker
城市选择器json  react-native-picker data 设置此json即可


let cityData = require("../../utils/city.json");

 //#region 城市选择初始化
    initPicker(){
        Picker.init({
            pickerTitleText: "选择城市",
            pickerConfirmBtnText: "确定",
            pickerCancelBtnText:"取消",
            pickerData: cityData,
            selectedValue:["北京市","北京市","东城区"],
            onPickerConfirm: data => {
                // Picker.hide();
                this.setState({cityTitle: data ==null ? "" : data[0] + data[1] + data[2]})
            },
            onpointercancel: data => {
                // Picker.hide();

            },
            onPickerSelect: data => {
                // Picker.hide();

            }
        })
        Picker.show();
    }
    //#endregion

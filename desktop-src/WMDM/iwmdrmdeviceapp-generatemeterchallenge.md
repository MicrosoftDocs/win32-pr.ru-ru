---
title: Метод Ивмдрмдевицеапп Женератеметерчалленже (Вмдрмдевицеапп. h)
description: Метод Женератеметерчалленже получает данные отслеживания использования с устройства.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Метод Женератеметерчалленже Windows Media диспетчер устройств
- Метод Женератеметерчалленже Windows Media диспетчер устройств, интерфейс Ивмдрмдевицеапп
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, метод Женератеметерчалленже
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695017"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a>Метод Ивмдрмдевицеапп:: Женератеметерчалленже

Метод **женератеметерчалленже** получает данные отслеживания использования с устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) . Если приложение передает **значение NULL**, то сведения об отслеживании, хранящиеся на компьютере, используются вместо сведений об отслеживании на подключенном устройстве.

</dd> <dt>

*бстрметерцерт* \[ окне\]
</dt> <dd>

Сертификат отслеживания приложения в виде **BSTR**. Это подписанный сертификат, полученный от корпорации Майкрософт.

</dd> <dt>

*пбстрметерурл* \[ заполняет\]
</dt> <dd>

URL-адрес, по которому должны отправляться данные измерения. Она выделяется Windows Media диспетчер устройств и должна быть свободна вызывающей стороной с помощью **сисфристринг**.

</dd> <dt>

*пбстрметердата* \[ заполняет\]
</dt> <dd>

Данные контроля использования для отправки в службу измерения. Она выделяется Windows Media диспетчер устройств и должна быть свободна вызывающей стороной с помощью **сисфристринг**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                      | Описание                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                             | Метод выполнен успешно.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                | Один или несколько аргументов недопустимы.<br/>                               |
| <dl> <dt>**DRM \_ E \_ инвалидксмлтаг**</dt> </dl>             | XML имеет неправильный формат.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ ноксмлклосетаг**</dt> </dl>             | XML имеет неправильный формат.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ ноксмлопентаг**</dt> </dl>              | XML имеет неправильный формат.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ ксмлнотфаунд**</dt> </dl>               | Не удалось найти требуемый XML-тег.<br/>                                 |
| <dl> <dt>**Ошибки с устройства**</dt> </dl>            | Любое количество ошибок на устройстве.<br/>                                  |
| <dl> <dt>**Ошибки клиента DRM**</dt> </dl>        | Любое количество внутренних ошибок клиента DRM.<br/>                     |
| <dl> <dt>**\_устройство NS E \_ не является \_ \_ \_ устройством WMDRM**</dt> </dl> | Указанное устройство не является устройством, совместимым с DRM Windows Media.<br/> |



 

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода приложение должно вызвать [**ивмдрмдевицеапп:: куеридевицестатус**](iwmdrmdeviceapp-querydevicestatus.md) или [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) , чтобы убедиться, что все компоненты DRM устройства обновлены. Этот метод может быть вызван только на устройстве, которое поддерживает Windows Media DRM 10 для переносных устройств.

Полученный *пбстрметердата* данных должен быть отправлен на URL-адрес, заданный параметром *пбстрметерурл*. Убедитесь, что извлеченные данные кодируются в URL-адресе, поэтому они не изменяются во время перемещения.

Дополнительные сведения см. [в разделе Обработка защищенного содержимого в приложении](handling-protected-content-in-the-application.md) .

## <a name="examples"></a>Примеры

В следующем примере кода C++ создается объект **вмдрмдевицеапп** , проверяется, является ли устройство устройством Windows Media DRM 10, что его часы точны, а затем запрашиваются данные о измерениях.


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмдевицеапп. h (также требуется Вмдрмдевицеапп \_ i. c, построенный из вмдрмдевицеапп. IDL)</dt> </dl> |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Обработка защищенного содержимого в приложении**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Интерфейс Ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Интерфейс Ивмдрмдевицеапп**](iwmdrmdeviceapp.md)
</dt> </dl>

 

 






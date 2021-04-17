---
title: Метод Ивмдрмдевицеапп Куеридевицестатус (Вмдрмдевицеапп. h)
description: Метод Куеридевицестатус запрашивает у устройства текущее состояние DRM и возможности.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Метод Куеридевицестатус Windows Media диспетчер устройств
- Метод Куеридевицестатус Windows Media диспетчер устройств, интерфейс Ивмдрмдевицеапп
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, метод Куеридевицестатус
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695015"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a>Метод Ивмдрмдевицеапп:: Куеридевицестатус

Метод **куеридевицестатус** запрашивает у устройства текущее состояние DRM и возможности.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Указатель на объект [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

</dd> <dt>

*пдвстатус* \[ заполняет\]
</dt> <dd>

Ноль или более следующих значений **DWORD** , ОПИСЫВАЮЩИХ аспекты DRM устройства, в сочетании с побитовым **или**. См. заметки.



| Состояние                      | Описание                                  |
|-----------------------------|----------------------------------------------|
| \_исвмдрм устройства \_ WMDRM      | Устройство поддерживает Windows Media DRM.       |
| \_нидклокк устройства \_ WMDRM    | Устройство не имеет безопасных часов.     |
| \_устройство WMDRM \_ отозвано      | Устройство было отозвано.                 |
| \_нидиндив клиента \_ WMDRM    | Необходимо выполнить индивидуальную защиту DRM. |
| \_рефрешклокк устройства \_ WMDRM | Необходимо обновить часы.             |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                              | Описание                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                     | Метод выполнен успешно.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ INVALIDARG**</dt> </dl>                        | Недопустимый входной аргумент.<br/>                               |
| <dl> <dt>**\_ \_ \_ Недопустимый \_ сертификат DRM в NS E**</dt> </dl>          | Сертификат устройства, полученный с устройства, является недопустимым.<br/> |
| <dl> <dt>**системе \_ \_ управления правами NS \_ не удалось \_ \_ получить \_ \_ сертификат устройства**</dt> </dl> | Не удалось получить сертификат устройства с устройства.<br/>     |



 

## <a name="remarks"></a>Комментарии

Этот метод следует вызывать перед выполнением каких либо ограниченных действий с содержимым DRM, например для передачи содержимого DRM на устройство или получения сведений о метриках. Если значения, полученные с помощью *пдвстатус* , указывают на необходимость выполнения какого-либо действия (например, для настольного компьютера или получения часов для устройства), приложение должно вызвать [**аккуиредевицедата**](iwmdrmdeviceapp-acquiredevicedata.md) и передать полученное значение *пдвстатус* из этой функции в параметр *dwFlags* в **аккуиредевицедата**. Если возвращается нуль, устройство не поддерживает Windows Media DRM 10 для переносных устройств, и никаких действий не требуется. Дополнительные сведения см. [в разделе Обработка защищенного содержимого в приложении](handling-protected-content-in-the-application.md) .

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

[**Интерфейс Ивмдрмдевицеапп**](iwmdrmdeviceapp.md)
</dt> <dt>

[**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 






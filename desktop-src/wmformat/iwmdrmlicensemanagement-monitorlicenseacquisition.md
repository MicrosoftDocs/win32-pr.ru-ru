---
title: Метод Ивмдрмлиценсеманажемент Мониторлиценсеаккуиситион (Вмдрмсдк. h)
description: Метод Мониторлиценсеаккуиситион инициирует мониторинг процесса получения лицензии.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Формат Windows Media, Мониторлиценсеаккуиситион метод
- Мониторлиценсеаккуиситион метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Мониторлиценсеаккуиситион
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ab3188425decca614ae104989fdc2f07930ac0de463e492be630a3fb54556e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027582"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>Метод Ивмдрмлиценсеманажемент:: Мониторлиценсеаккуиситион

Метод **мониторлиценсеаккуиситион** инициирует мониторинг процесса получения лицензии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстркид* \[ окне\]
</dt> <dd>

Идентификатор ключа (ребенок) получаемой лицензии.

</dd> <dt>

*бстрхеадер* \[ окне\]
</dt> <dd>

Заголовок содержимого, который использовался при вызове метода [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .

</dd> <dt>

*бстрактионс* \[ окне\]
</dt> <dd>

Строка, содержащая действия, запрошенные при вызове метода **AcquireLicense** .

</dd> <dt>

*ппункканцелатионкукие* \[ заполняет\]
</dt> <dd>

Указатель, получающий указатель на интерфейс **IUnknown** объекта, определяющий этот асинхронный вызов. Этот указатель интерфейса можно использовать для отмены асинхронного вызова путем вызова метода [**ивмдрмевентженератор:: канцеласинкоператион**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмдрмлиценсеманажемент**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 






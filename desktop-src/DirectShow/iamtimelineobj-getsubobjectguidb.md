---
description: 'Метод Жетсубобжектгуидб извлекает идентификатор GUID для подобъекта, связанного с этим объектом временной шкалы. Этот метод эквивалентен Иамтимелинеобж:: Жетсубобжектгуид, но получает значение BSTR.'
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'Метод Иамтимелинеобж:: Жетсубобжектгуидб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79cf7c6a0b3f162f3f3baee2a46cfc0c2c2b61271b19e57549c73b4faa0594bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155385"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a>Метод Иамтимелинеобж:: Жетсубобжектгуидб

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetSubObjectGUIDB`Метод получает идентификатор GUID подобъекта, связанного с этим объектом временной шкалы. Этот метод эквивалентен [**иамтимелинеобж:: жетсубобжектгуид**](iamtimelineobj-getsubobjectguid.md), но получает значение **BSTR** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает строку, представляющую GUID подобъекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Метод выделяет память для строки. Приложение должно вызвать **сисфристринг** для освобождения памяти.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинеобж**](iamtimelineobj.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: Запрос на обновление первоначального состояния объекта; Например, текстура или шейдер.
MS-HAID: vspixengine.IUpdateObject\_UpdateObject\_UINT\_DWORD\_BYTE\_arr\_IUpdateObjectCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иупдатеобжект:: UpdateObject'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 824AB599-7377-4F77-8FC8-41E17ED57A79
api_name:
- IUpdateObject.UpdateObject
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b04918878de15a2b9a5b004d3dff252ab3ddc9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495252"
---
# <a name="span-idvspixengineiupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptrspaniupdateobjectupdateobject-method"></a><span id="vspixengine.iupdateobject_updateobject_uint_dword_byte_arr_iupdateobjectcallback_ptr"></span>Метод Иупдатеобжект:: UpdateObject

Запрос на обновление первоначального состояния объекта; Например, текстура или шейдер.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UpdateObject(
   UINT                    objectAddress,
   DWORD                   size,
   BYTE []                 count1_buffer,
   IUpdateObjectCallback * pCallback
);
```

## <a name="parameters"></a>Параметры

*обжектаддресс*   
Идентификатор обновляемого объекта.

*изменять*   
Размер полезных данных обновления в байтах.

*\_буфер count1*   
Полезные данные обновления.

*пкаллбакк*   
Адрес функции, используемой для уведомления узла о том, что объект был обновлен.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иупдатеобжект**](/windows/desktop/direct3dtools/iupdateobject)

 

 

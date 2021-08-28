---
description: Передает ресурсы в подсистему, например строки для сообщений об ошибках.
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine3:: Сетупресаурцес'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1BB4BE17-51A2-4BA4-81F5-3678B7D5802B
api_name:
- IPixEngine3.SetupResources
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c33bb9eea38575fa3acb4a94b926f9cce1af250
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628160"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>Метод IPixEngine3:: Сетупресаурцес

Передает ресурсы в подсистему, например строки для сообщений об ошибках.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a>Параметры

*\_ресурсы count1*   
Переданные ресурсы ресурсов.

*расчета*   
Число переданных ресурсов.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine3**](/windows/desktop/direct3dtools/ipixengine3)

 

 

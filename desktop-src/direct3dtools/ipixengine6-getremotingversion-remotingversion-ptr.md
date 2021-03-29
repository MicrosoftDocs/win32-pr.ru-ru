---
description: Возвращает версию компонента для удаленного взаимодействия.
MS-HAID: vspixengine.IPixEngine6\_GetRemotingVersion\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine6:: Жетремотингверсион'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 065FC3A7-ECFB-4551-B4B0-CA0E6B8676F8
api_name:
- IPixEngine6.GetRemotingVersion
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85230a71d9c0f2dd437ec25af3eb6c660f032586
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072248"
---
# <a name="span-idvspixengineipixengine6_getremotingversion_remotingversion_ptrspanipixengine6getremotingversion-method"></a><span id="vspixengine.ipixengine6_getremotingversion_remotingversion_ptr"></span>Метод IPixEngine6:: Жетремотингверсион

Возвращает версию компонента для удаленного взаимодействия.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRemotingVersion(
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a>Параметры

*премотеверсион*   
Версия модуля удаленного взаимодействия.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine6**](/windows/desktop/direct3dtools/ipixengine6)

 

 

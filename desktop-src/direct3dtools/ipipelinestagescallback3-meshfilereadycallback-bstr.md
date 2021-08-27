---
description: Обратный вызов, уведомляющий узел о размещении сведений о сетке, записанных связанным запросом.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPipeLineStagesCallback3:: Мешфилереадикаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c695ebad2f8a23757419fe3c6894a91b00cbd2d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625150"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>Метод IPipeLineStagesCallback3:: Мешфилереадикаллбакк

Обратный вызов, уведомляющий узел о размещении сведений о сетке, записанных связанным запросом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a>Параметры

*мешфиленаме*   
Строка COM, содержащая путь к файлу, в который записываются данные сетки.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPipeLineStagesCallback3**](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 

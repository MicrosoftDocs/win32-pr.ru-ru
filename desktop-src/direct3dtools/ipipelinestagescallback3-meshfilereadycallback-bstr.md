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
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673007"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPipeLineStagesCallback3**](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 

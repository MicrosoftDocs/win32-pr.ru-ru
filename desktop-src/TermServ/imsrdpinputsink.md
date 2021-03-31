---
title: Интерфейс Имсрдпинпутсинк
description: Приемник входных данных удаленного рабочего стола.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпинпутсинк
- Службы удаленных рабочих столов интерфейса Имсрдпинпутсинк, описание
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988403"
---
# <a name="imsrdpinputsink-interface"></a>Интерфейс Имсрдпинпутсинк

Приемник входных данных удаленного рабочего стола.

## <a name="members"></a>Элементы

Интерфейс **имсрдпинпутсинк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Имсрдпинпутсинк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **имсрдпинпутсинк** содержит следующие методы.



| Метод                                                               | Описание                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**аддтаучинпут**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | Добавляет сенсорный ввод.<br/>         |
| [**бегинтаучфраме**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | Начало рамки касания.<br/>        |
| [**ендтаучфраме**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | Конечный кадр касания.<br/>          |
| [**сендкэйбоардевент**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | Отправляет событие клавиатуры.<br/>     |
| [**сендмаусебуттоневент**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | Отправляет событие кнопки мыши.<br/> |
| [**сендмаусемовивент**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | Отправляет событие перемещения указателя мыши.<br/>   |
| [**сендмаусевхилевент**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | Отправляет событие колесика мыши.<br/>  |
| [**сендсинцевент**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | Отправляет событие синхронизации.<br/>         |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                      |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпинпутсинк определен как 4606850E-76A7-4E28-A47E-C7174F619351<br/>     |



 


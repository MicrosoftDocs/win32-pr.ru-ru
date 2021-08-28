---
description: Перечисление, используемое для отправки ответов от подсистемы захвата к диагностика графики.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление Пикспипереспонсе
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ad00d7bada935dd27f711499e5975d31709b9940
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631692"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Перечисление Пикспипереспонсе

Перечисление, используемое для отправки ответов от подсистемы захвата к диагностика графики.

## <a name="syntax"></a>Синтаксис


```C++
};
```

## <a name="constants"></a>Константы

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**\_доступны новые данные \_**  
Ответ, указывающий, что новые данные были записаны в журнал графики и готовы к чтению.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**данные ЭКСПЕРИМЕНТа \_**  
Ответ, который указывает сведения о конфигурации сеанса записи.

<span id="ERRORCODE"></span><span id="errorcode"></span>**КОД ошибки**  
Ответ, указывающий, что в подсистеме записи обнаружена ошибка.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**аппликатионкаптуреинпрогресс**  
Ответ, указывающий, что подсистема отслеживания начала запись графических данных. Это не означает, что данные будут доступны для анализа.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**ЧАСТИЧные \_ данные**  
Ответ, указывающий, что в журнал графики записаны частичные данные.

<span id="READY"></span><span id="ready"></span>**ВСЁ**  
Ответ, указывающий, что подсистема отслеживания готова начать запись графических данных.

<span id="DONE"></span><span id="done"></span>**ДОГОВОРИЛИСЬ**  
Внутренние

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**каптурестартед**  
Ответ, указывающий на начало записи кадров.

<span id="STATUS"></span><span id="status"></span>**СОСТОЯНИЕ**  
Ответ, который указывает сведения о состоянии собираемого приложения; Например, частота кадров.

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 




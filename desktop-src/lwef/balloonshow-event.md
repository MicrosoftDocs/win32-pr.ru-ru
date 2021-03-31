---
title: Событие Баллуншов
description: Событие Баллуншов
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411214"
---
# <a name="balloonshow-event"></a>Событие Баллуншов

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит при отображении всплывающего окна символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Подагент* \_ **баллуншов** **(ByVal** *чарактерид * *)**



| Отделение          | Описание                                                       |
|---------------|-------------------------------------------------------------------|
| *чарактерид* | Возвращает идентификатор символа, связанного со всплывающей подсказкой. |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Сервер отправляет это событие только клиентам символа (приложения, которые загрузили символ), который использует всплывающую подсказку Word.

### <a name="see-also"></a>См. также:

[**Событие Баллунхиде**](balloonhide-event.md)


 

 





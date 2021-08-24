---
title: Событие Баллуншов
description: Событие Баллуншов
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10aa8ab2c556fdf603a3972033a7440041fef6a45f828115c649a8a42810eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726144"
---
# <a name="balloonshow-event"></a>Событие Баллуншов

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Происходит при отображении всплывающего окна символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 *Подагент* \_ **баллуншов** **(ByVal** *чарактерид * *)**



| Часть          | Описание                                                       |
|---------------|-------------------------------------------------------------------|
| *чарактерид* | Возвращает идентификатор символа, связанного со всплывающей подсказкой. |



 

</dd> </dl>

### <a name="remarks"></a>Remarks

Сервер отправляет это событие только клиентам символа (приложения, которые загрузили символ), который использует всплывающую подсказку Word.

### <a name="see-also"></a>См. также:

[**Событие Баллунхиде**](balloonhide-event.md)


 

 





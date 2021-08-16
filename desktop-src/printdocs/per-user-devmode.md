---
description: Пользователь может указать параметры документа по умолчанию для принтера. Это называется DEVMODE для каждого пользователя, так как он влияет только на значения по умолчанию для конкретного пользователя, а сведения для каждого принтера определяются в отдельной структуре DEVMODE.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5e9fd2872d055dba6d04f060e6d2e581e461fd20ddc418f643d09170cda31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731932"
---
# <a name="per-user-devmode"></a>Per-User DEVMODE

Пользователь может указать параметры документа по умолчанию для принтера. Это называется DEVMODE для *каждого пользователя* , так как он влияет только на значения по умолчанию для конкретного пользователя, а сведения для каждого принтера определяются в отдельной структуре [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .

Чтобы задать DEVMODE для каждого пользователя, вызовите [**сетпринтер**](setprinter.md) со структурой [**Printer \_ info \_ 2**](printer-info-2.md) или [**Printer \_ info \_ 9**](printer-info-9.md) . Чтобы сбросить DEVMODE для каждого пользователя до глобального [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)по умолчанию, вызовите **сетпринтер** с помощью структуры [**Printer \_ info \_ 8**](printer-info-8.md) .

 

 




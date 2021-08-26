---
description: Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графика или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled функции контекста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33337aeea32f1ca84b74e3fc45e9bd67dbfe1ce1a5300a502a5303f55cab357
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944204"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled функции контекста устройства

Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графика или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств. (дополнительные сведения см. в разделе [Windows цветовая система](/previous-versions//dd372446(v=vs.85)).)

В интерфейсе графических устройств (GDI) есть различные функции, которые используют данные цвета или работают с ними. Следующие функции контекста устройства включены для использования с ICM:

-   [**креатекомпатибледк**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**жетдкбрушколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**жетдкпенколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ресетдк**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**Функцию**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**сетдкбрушколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**сетдкпенколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 

---
description: Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графика или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled функции контекста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984952"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled функции контекста устройства

Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графика или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств. (Дополнительные сведения см. в разделе [Цветовая система Windows](/previous-versions//dd372446(v=vs.85)).)

В интерфейсе графических устройств (GDI) есть различные функции, которые используют данные цвета или работают с ними. Следующие функции контекста устройства включены для использования с ICM:

-   [**креатекомпатибледк**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**жетдкбрушколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**жетдкпенколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ресетдк**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**Функцию**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**сетдкбрушколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**сетдкпенколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 

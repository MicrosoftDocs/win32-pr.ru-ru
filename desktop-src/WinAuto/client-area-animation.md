---
title: Параметр анимации в клиентской области
description: Флаг анимации в клиентской области показывает, хочет ли пользователь отключить анимацию в элементах пользовательского интерфейса.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104261002"
---
# <a name="client-area-animation-parameter"></a><span data-ttu-id="5192d-103">Параметр анимации в клиентской области</span><span class="sxs-lookup"><span data-stu-id="5192d-103">Client area animation parameter</span></span>

<span data-ttu-id="5192d-104">Параметр анимации клиентской области указывает, хочет ли пользователь отключить анимацию в элементах пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5192d-104">The client area animation parameter indicates whether the user wants to disable animations in UI elements.</span></span> <span data-ttu-id="5192d-105">Отображение таких функций, как мигающий, мигающий, мерцание и перемещение содержимого, может привести к захвату пользователей с епилепси, учитывающими фотографию.</span><span class="sxs-lookup"><span data-stu-id="5192d-105">Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy.</span></span> <span data-ttu-id="5192d-106">Этот параметр позволяет включить или отключить все такие анимации.</span><span class="sxs-lookup"><span data-stu-id="5192d-106">This parameter enables you to enable or disable all such animations.</span></span>

<span data-ttu-id="5192d-107">Приложения используют флаги **SPI \_ Жетклиентареааниматион** и **SPI \_ сетклиентареааниматион** с функцией [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) для включения или отключения анимации в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="5192d-107">Applications use the **SPI\_GETCLIENTAREAANIMATION** and **SPI\_SETCLIENTAREAANIMATION** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to turn client area animations on or off.</span></span>

 

 
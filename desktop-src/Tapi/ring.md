---
description: Один телефон может иметь возможность звонить с различными режимами кольца.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Кольцо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998471"
---
# <a name="ring"></a><span data-ttu-id="2acdc-103">Кольцо</span><span class="sxs-lookup"><span data-stu-id="2acdc-103">Ring</span></span>

<span data-ttu-id="2acdc-104">Один телефон может иметь возможность звонить с различными режимами кольца.</span><span class="sxs-lookup"><span data-stu-id="2acdc-104">A single phone may be able to ring with different ring modes.</span></span> <span data-ttu-id="2acdc-105">При наличии широкого спектра доступных режимов звонка режимы звонка определяются с помощью номера режима кольца.</span><span class="sxs-lookup"><span data-stu-id="2acdc-105">Given the wide variety of ring modes available, ring modes are identified by means of their ring mode number.</span></span> <span data-ttu-id="2acdc-106">Число в режиме кольца в диапазоне от нуля до числа доступных режимов звонка минус один.</span><span class="sxs-lookup"><span data-stu-id="2acdc-106">A ring mode number ranges from zero to the number of available ring modes minus one.</span></span>

<span data-ttu-id="2acdc-107">Функции, которые приложение будет использовать для управления режимами звонка телефонного устройства, — это [**фонесетринг**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), которые обзвонт открытое устройство в соответствии с заданным режимом кольца, и [**фонежетринг**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), который возвращает текущий режим звонка открытого телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="2acdc-107">The functions an application would use to control a phone device's ring modes are [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), which rings an open phone device according to a given ring mode, and [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), which returns the current ring mode of an opened phone device.</span></span>

<span data-ttu-id="2acdc-108">При изменении режима кольца телефонного устройства в приложение отправляется сообщение [**о \_ состоянии телефона**](phone-state.md) , чтобы уведомить приложение об изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="2acdc-108">When the ring mode of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="2acdc-109">Параметры этого сообщения содержат сведения об изменении.</span><span class="sxs-lookup"><span data-stu-id="2acdc-109">Parameters to this message provide an indication of the change.</span></span>

 

 




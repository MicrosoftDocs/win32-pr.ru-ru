---
description: Система поддерживает кэш отображаемых контекстов устройств, которые используются для общих, родительских и оконных контекстов устройств.
ms.assetid: b017453a-c2c5-4bb1-ae46-f303d5e200ca
title: Отображение кэша контекста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd9149d4c4ffed6b25f3eb40d0fd9b1ffca1bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997410"
---
# <a name="display-device-context-cache"></a><span data-ttu-id="a2445-103">Отображение кэша контекста устройства</span><span class="sxs-lookup"><span data-stu-id="a2445-103">Display Device Context Cache</span></span>

<span data-ttu-id="a2445-104">Система поддерживает кэш отображаемых контекстов устройств, которые используются для общих, родительских и оконных контекстов устройств.</span><span class="sxs-lookup"><span data-stu-id="a2445-104">The system maintains a cache of display device contexts that it uses for common, parent, and window device contexts.</span></span> <span data-ttu-id="a2445-105">Система получает контекст устройства из кэша всякий раз, когда приложение вызывает функцию [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) или [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . система возвращает контроллер домена в кэш, когда приложение впоследствии вызывает функцию [**релеаседк**](/windows/desktop/api/Winuser/nf-winuser-releasedc) или [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .</span><span class="sxs-lookup"><span data-stu-id="a2445-105">The system retrieves a device context from the cache whenever an application calls the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) function; the system returns the DC to the cache when the application subsequently calls the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) or [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) function.</span></span>

<span data-ttu-id="a2445-106">Не существует заранее определенного ограничения на количество контекстов устройств, которые может хранить кэш. система создает новый контекст устройства просмотра для кэша, если он отсутствует.</span><span class="sxs-lookup"><span data-stu-id="a2445-106">There is no predetermined limit on the amount of device contexts that a cache can hold; the system creates a new display device context for the cache if none is available.</span></span> <span data-ttu-id="a2445-107">Учитывая это, приложение может иметь более пяти активных контекстов устройств из кэша за раз.</span><span class="sxs-lookup"><span data-stu-id="a2445-107">Given this, an application can have more than five active device contexts from the cache at a time.</span></span> <span data-ttu-id="a2445-108">Однако приложение должно продолжать освобождать эти контексты устройств после использования.</span><span class="sxs-lookup"><span data-stu-id="a2445-108">However, the application must continue to release these device contexts after use.</span></span> <span data-ttu-id="a2445-109">Так как новые контексты дисплея для кэша выделяются в пространстве кучи приложения, не освобождая контексты устройств в конечном итоге потребляют всю доступную область кучи.</span><span class="sxs-lookup"><span data-stu-id="a2445-109">Because new display device contexts for the cache are allocated in the application's heap space, failing to release the device contexts eventually consumes all available heap space.</span></span> <span data-ttu-id="a2445-110">Система указывает на этот сбой, возвращая ошибку, если ей не удается выделить место для нового контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="a2445-110">The system indicates this failure by returning an error when it cannot allocate space for the new device context.</span></span> <span data-ttu-id="a2445-111">Другие функции, не связанные с кэшем, также могут возвращать ошибки.</span><span class="sxs-lookup"><span data-stu-id="a2445-111">Other functions unrelated to the cache may also return errors.</span></span>

 

 




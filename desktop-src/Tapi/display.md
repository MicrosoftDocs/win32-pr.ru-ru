---
description: Интерфейс TAPI предоставляет доступ к телефонам.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Отображение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145238"
---
# <a name="display"></a><span data-ttu-id="d39ec-103">Отображение</span><span class="sxs-lookup"><span data-stu-id="d39ec-103">Display</span></span>

<span data-ttu-id="d39ec-104">TAPI обеспечивает доступ к дисплею телефона.</span><span class="sxs-lookup"><span data-stu-id="d39ec-104">TAPI provides access to a phone's display.</span></span> <span data-ttu-id="d39ec-105">Отображение моделируется как буквенно-цифровая область с строками и столбцами.</span><span class="sxs-lookup"><span data-stu-id="d39ec-105">The display is modeled as an alphanumeric area with rows and columns.</span></span> <span data-ttu-id="d39ec-106">Возможности устройства для телефона указывают размер отображения телефона в виде числа строк и количества столбцов.</span><span class="sxs-lookup"><span data-stu-id="d39ec-106">A phone's device capabilities indicate the size of a phone's display as the number of rows and the number of columns.</span></span> <span data-ttu-id="d39ec-107">Оба эти числа равны нулю, если у телефонного устройства нет экрана.</span><span class="sxs-lookup"><span data-stu-id="d39ec-107">Both these numbers are zero if the phone device does not have a display.</span></span> <span data-ttu-id="d39ec-108">Используйте [**фонесетдисплай**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) для записи информации на устройство с открытым телефоном и [**фонежетдисплай**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) для получения текущего содержимого экрана телефона.</span><span class="sxs-lookup"><span data-stu-id="d39ec-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) to write information to the display of an open phone device, and [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) to retrieve the current contents of a phone's display.</span></span>

<span data-ttu-id="d39ec-109">При изменении отображения телефонного устройства в функцию приложения отправляется сообщение о [**\_ состоянии телефона**](phone-state.md) , чтобы уведомить приложение об изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="d39ec-109">When the display of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="d39ec-110">Параметры этого сообщения содержат сведения об изменении.</span><span class="sxs-lookup"><span data-stu-id="d39ec-110">Parameters to this message provide an indication of the change.</span></span>

 

 




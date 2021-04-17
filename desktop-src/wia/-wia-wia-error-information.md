---
description: API-интерфейсы для получения образа Windows (WIA) возвращают состояние завершения в возвращаемом значении HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Сведения об ошибке WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711084"
---
# <a name="wia-error-information"></a><span data-ttu-id="8b4c8-103">Сведения об ошибке WIA</span><span class="sxs-lookup"><span data-stu-id="8b4c8-103">WIA Error Information</span></span>

<span data-ttu-id="8b4c8-104">API-интерфейсы для получения образа Windows (WIA) возвращают состояние завершения в возвращаемом значении HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-104">The Windows Image Acquisition (WIA)APIs return their completion status in an HRESULT return value.</span></span> <span data-ttu-id="8b4c8-105">Приложения проверяют эти возвращаемые значения \_ на основе константы WIA, чтобы определить, требует ли ошибка вмешательство пользователя для очистки, например подачи бумаги с застреванием на бумаге, и сообщите о ней пользователю.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-105">Applications check these return values against the FACILITY\_WIA constant to determine whether the error requires user intervention to clear, such as a jammed paper path, and report them to the user.</span></span> <span data-ttu-id="8b4c8-106">Кроме того, все ошибки на уровне драйверов записываются в журнал событий с помощью строк ошибок, предоставленных минидривером устройства.</span><span class="sxs-lookup"><span data-stu-id="8b4c8-106">In addition, all driver-level errors are logged in detail to the event log, using error strings provided by the device minidriver.</span></span> <span data-ttu-id="8b4c8-107">Список кодов ошибок, связанных с WIA, см. в разделе [коды ошибок](-wia-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8b4c8-107">For a listing of WIA-specific error codes, see [Error Codes](-wia-error-codes.md).</span></span>

 

 




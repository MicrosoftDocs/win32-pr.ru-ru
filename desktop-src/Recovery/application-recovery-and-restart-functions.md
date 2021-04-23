---
title: Функции восстановления и перезапуска приложений
description: Восстановление и перезапуск приложений определяет следующие функции.
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134270"
---
# <a name="application-recovery-and-restart-functions"></a><span data-ttu-id="1b7b4-103">Функции восстановления и перезапуска приложений</span><span class="sxs-lookup"><span data-stu-id="1b7b4-103">Application Recovery and Restart Functions</span></span>

<span data-ttu-id="1b7b4-104">Восстановление и перезапуск приложений определяет следующие функции:</span><span class="sxs-lookup"><span data-stu-id="1b7b4-104">Application Recovery and Restart defines the following functions:</span></span>



| <span data-ttu-id="1b7b4-105">Функция</span><span class="sxs-lookup"><span data-stu-id="1b7b4-105">Function</span></span>                                                                               | <span data-ttu-id="1b7b4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1b7b4-106">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b7b4-107">**аппликатионрековерифинишед**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-107">**ApplicationRecoveryFinished**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | <span data-ttu-id="1b7b4-108">Указывает, что вызывающее приложение завершило восстановление данных.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-108">Indicates that the calling application has completed its data recovery.</span></span>                    |
| [<span data-ttu-id="1b7b4-109">**аппликатионрековеринпрогресс**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-109">**ApplicationRecoveryInProgress**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | <span data-ttu-id="1b7b4-110">Указывает, что вызывающее приложение продолжает восстанавливать данные.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-110">Indicates that the calling application is continuing to recover data.</span></span>                      |
| [<span data-ttu-id="1b7b4-111">**жетаппликатионрековерикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-111">**GetApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | <span data-ttu-id="1b7b4-112">Возвращает указатель на подпрограммы обратного вызова восстановления, зарегистрированную для указанного процесса.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-112">Retrieves a pointer to the recovery callback routine registered for the specified process.</span></span> |
| [<span data-ttu-id="1b7b4-113">**жетаппликатионрестартсеттингс**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-113">**GetApplicationRestartSettings**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | <span data-ttu-id="1b7b4-114">Извлекает сведения о перезапуске, зарегистрированные для указанного процесса.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-114">Retrieves the restart information registered for the specified process.</span></span>                    |
| [<span data-ttu-id="1b7b4-115">**регистераппликатионрековерикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-115">**RegisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | <span data-ttu-id="1b7b4-116">Регистрирует активный экземпляр приложения для восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-116">Registers the active instance of an application for recovery.</span></span>                              |
| [<span data-ttu-id="1b7b4-117">**регистераппликатионрестарт**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-117">**RegisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | <span data-ttu-id="1b7b4-118">Регистрирует активный экземпляр приложения для перезапуска.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-118">Registers the active instance of an application for restart.</span></span>                               |
| [<span data-ttu-id="1b7b4-119">**унрегистераппликатионрековерикаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-119">**UnregisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | <span data-ttu-id="1b7b4-120">Удаляет активный экземпляр приложения из списка восстановления.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-120">Removes the active instance of an application from the recovery list.</span></span>                      |
| [<span data-ttu-id="1b7b4-121">**унрегистераппликатионрестарт**</span><span class="sxs-lookup"><span data-stu-id="1b7b4-121">**UnregisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | <span data-ttu-id="1b7b4-122">Удаляет активный экземпляр приложения из списка перезапуска.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-122">Removes the active instance of an application from the restart list.</span></span>                       |



 

 

 
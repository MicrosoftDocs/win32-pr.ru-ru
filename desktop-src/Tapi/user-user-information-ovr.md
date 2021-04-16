---
description: Сведения о пользователе — это буфер, который может быть передан из одного конца соединения в другое. Эти сведения относятся к стандарту ISDN Q. 931. Ознакомьтесь с документацией поставщиков услуг по значению и использованию этих данных.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Сведения о пользователе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546298"
---
# <a name="user-user-information"></a><span data-ttu-id="866ab-105">Сведения о пользователе</span><span class="sxs-lookup"><span data-stu-id="866ab-105">User-user information</span></span>

<span data-ttu-id="866ab-106">Сведения о пользователе — это буфер, который может быть передан из одного конца соединения в другое.</span><span class="sxs-lookup"><span data-stu-id="866ab-106">User-user information is a buffer that can be transmitted from one end of a connection to another.</span></span> <span data-ttu-id="866ab-107">Эти сведения относятся к стандарту ISDN Q. 931.</span><span class="sxs-lookup"><span data-stu-id="866ab-107">This information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="866ab-108">Ознакомьтесь с документацией поставщика услуг по значению и использованию этих данных.</span><span class="sxs-lookup"><span data-stu-id="866ab-108">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="866ab-109">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="866ab-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="866ab-110">\* \* TAPI 2. x: \* \*[**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двкаллдатасизе** и **двкаллдатаоффсет** члены [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**линесендусерусеринфо**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="866ab-110">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span></span>

<span data-ttu-id="866ab-111">\* \* TAPI 3. x: \* \*[**иткаллинфо:: жеткаллинфобуффер**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), вызванный с элементом **ЦИБ \_ усерусеринфо** в [**Каллинфо \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**иткаллинфо:: релеасеусерусеринфо**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="866ab-111">\*\*TAPI 3.x:  \*\*[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), called with the **CIB\_USERUSERINFO** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span></span>

 

 

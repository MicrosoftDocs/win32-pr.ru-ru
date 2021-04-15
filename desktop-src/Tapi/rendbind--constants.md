---
description: 'Константы РЕНДБИНД — это флаги, используемые методом Итдиректори:: BIND для обозначения типов предоставленной проверки подлинности.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Константы RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689119"
---
# <a name="rendbind_-constants"></a><span data-ttu-id="27dc5-103">\_Константы рендбинд</span><span class="sxs-lookup"><span data-stu-id="27dc5-103">RENDBIND\_ Constants</span></span>

<span data-ttu-id="27dc5-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="27dc5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="27dc5-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="27dc5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="27dc5-106">Константы РЕНДБИНД — это флаги, используемые методом [**итдиректори:: BIND**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) для обозначения типов предоставленной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="27dc5-106">The RENDBIND constants are flags used by the [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) method to indicate types of authentication supplied.</span></span>

<dl> <dt>

<span data-ttu-id="27dc5-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**\_Проверка подлинности рендбинд**</span><span class="sxs-lookup"><span data-stu-id="27dc5-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="27dc5-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27dc5-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="27dc5-109">Проверка подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="27dc5-109">Authenticate user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="27dc5-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**РЕНДБИНД \_ дефаултдомаиннаме**</span><span class="sxs-lookup"><span data-stu-id="27dc5-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND\_DEFAULTDOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="27dc5-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="27dc5-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="27dc5-112">Использовать доменное имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27dc5-112">Use default domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="27dc5-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**РЕНДБИНД \_ дефаултусернаме**</span><span class="sxs-lookup"><span data-stu-id="27dc5-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND\_DEFAULTUSERNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="27dc5-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="27dc5-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="27dc5-115">Использовать имя пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27dc5-115">Use default user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="27dc5-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**РЕНДБИНД \_ DEFAULTPASSWORD**</span><span class="sxs-lookup"><span data-stu-id="27dc5-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND\_DEFAULTPASSWORD**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="27dc5-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="27dc5-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="27dc5-118">Использовать пароль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27dc5-118">Use default password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="27dc5-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**РЕНДБИНД \_ дефаулткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="27dc5-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND\_DEFAULTCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="27dc5-120">0x0000000e</span><span class="sxs-lookup"><span data-stu-id="27dc5-120">0x0000000e</span></span>
</dt> <dt>



<span data-ttu-id="27dc5-121">Предыдущие три ORed вместе для удобства.</span><span class="sxs-lookup"><span data-stu-id="27dc5-121">The previous three ORed together for convenience.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27dc5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="27dc5-122">Requirements</span></span>



| <span data-ttu-id="27dc5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="27dc5-123">Requirement</span></span> | <span data-ttu-id="27dc5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="27dc5-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="27dc5-125">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="27dc5-125">TAPI version</span></span><br/> | <span data-ttu-id="27dc5-126">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="27dc5-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="27dc5-127">Header</span><span class="sxs-lookup"><span data-stu-id="27dc5-127">Header</span></span><br/>       | <dl> <span data-ttu-id="27dc5-128"><dt>Rend. h</dt></span><span class="sxs-lookup"><span data-stu-id="27dc5-128"><dt>Rend.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27dc5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27dc5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27dc5-130">**итдиректори**</span><span class="sxs-lookup"><span data-stu-id="27dc5-130">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="27dc5-131">**Итдиректори:: BIND**</span><span class="sxs-lookup"><span data-stu-id="27dc5-131">**ITDirectory::Bind**</span></span>](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 





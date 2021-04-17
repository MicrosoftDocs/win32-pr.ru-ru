---
description: В следующем списке содержатся методы внутреннего адреса КМСП.
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: Внутренние вспомогательные методы Кмспаддресс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684672"
---
# <a name="cmspaddress-internal-helper-methods"></a><span data-ttu-id="83d99-103">Внутренние вспомогательные методы Кмспаддресс</span><span class="sxs-lookup"><span data-stu-id="83d99-103">CMSPAddress Internal Helper Methods</span></span>



| <span data-ttu-id="83d99-104">Внутренние вспомогательные методы Кмспаддресс</span><span class="sxs-lookup"><span data-stu-id="83d99-104">CMSPAddress internal helper methods</span></span>                                        | <span data-ttu-id="83d99-105">Описание</span><span class="sxs-lookup"><span data-stu-id="83d99-105">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83d99-106">**жетстатиктерминалс**</span><span class="sxs-lookup"><span data-stu-id="83d99-106">**GetStaticTerminals**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | <span data-ttu-id="83d99-107">Вызывается [**Get \_ Статиктерминалс**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) и [**енумератестатиктерминалс**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) для получения массива статических терминалов, которые могут использоваться по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="83d99-107">Called by [**get\_StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) and [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) to get an array of static terminals that can be used on this address.</span></span>                                     |
| [<span data-ttu-id="83d99-108">**жетдинамиктерминалклассес**</span><span class="sxs-lookup"><span data-stu-id="83d99-108">**GetDynamicTerminalClasses**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | <span data-ttu-id="83d99-109">Вызывается [**Get \_ Динамиктерминалклассес**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) и [**енумератединамиктерминалклассес**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) для получения массива динамических классов терминала, которые могут использоваться по этому адресу.</span><span class="sxs-lookup"><span data-stu-id="83d99-109">Called by [**get\_DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) and [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) to get an array of dynamic terminal classes that can be used on this address.</span></span> |
| [<span data-ttu-id="83d99-110">**упдатетерминаллист**</span><span class="sxs-lookup"><span data-stu-id="83d99-110">**UpdateTerminalList**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | <span data-ttu-id="83d99-111">Заполнение списка MSP статических терминалов.</span><span class="sxs-lookup"><span data-stu-id="83d99-111">Populates the MSP's list of static terminals.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="83d99-112">**рецеиветспаддрессдата**</span><span class="sxs-lookup"><span data-stu-id="83d99-112">**ReceiveTSPAddressData**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | <span data-ttu-id="83d99-113">Вызывается, когда сообщение данных TSP должно обрабатываться адресом, а не конкретным вызовом.</span><span class="sxs-lookup"><span data-stu-id="83d99-113">Called when a TSP data message is intended to be processed by the address rather than by a specific call.</span></span>                                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="83d99-114">См. также</span><span class="sxs-lookup"><span data-stu-id="83d99-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83d99-115">**кмспаддресс**</span><span class="sxs-lookup"><span data-stu-id="83d99-115">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 

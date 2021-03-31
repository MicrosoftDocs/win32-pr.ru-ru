---
description: 'Если вы используете COM API для WMI для извлечения или хранения сведений о локализованном классе, укажите языковой стандарт в параметре Стрлокале для интерфейса Ивбемлокатор:: Коннектсервер.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Получение измененных классов с помощью API COM для WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818040"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a><span data-ttu-id="144cb-103">Получение измененных классов с помощью API COM для WMI</span><span class="sxs-lookup"><span data-stu-id="144cb-103">Retrieving Amended Classes Using the COM API for WMI</span></span>

<span data-ttu-id="144cb-104">Если вы используете COM API для WMI для извлечения или хранения сведений о локализованном классе, укажите языковой стандарт в параметре *стрлокале* для интерфейса [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="144cb-104">If you are using the COM API for WMI to retrieve or store localized class information, specify the locale in the *strLocale* parameter to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) interface.</span></span> <span data-ttu-id="144cb-105">При чтении или записи измененных классов укажите, что вы хотите использовать локализованные определения классов, указав \_ флаг \_ WBEM \_ . в \_ качестве флага для параметра *ифлагс* следует использовать измененные квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="144cb-105">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS as a flag for the *iFlags* parameter.</span></span>

<span data-ttu-id="144cb-106">В следующей таблице перечислены синхронные и асинхронные версии методов, использующих \_ флаг WBEM \_ , \_ флаг измененных \_ квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="144cb-106">The following table lists the synchronous and asynchronous versions of the methods that use the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span>



| <span data-ttu-id="144cb-107">Синхронный метод</span><span class="sxs-lookup"><span data-stu-id="144cb-107">Synchronous Method</span></span>                                                            | <span data-ttu-id="144cb-108">Асинхронный метод</span><span class="sxs-lookup"><span data-stu-id="144cb-108">Asynchronous Method</span></span>                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="144cb-109">**IWbemServices:: Креатеклассенум**</span><span class="sxs-lookup"><span data-stu-id="144cb-109">**IWbemServices::CreateClassEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [<span data-ttu-id="144cb-110">**IWbemServices:: Креатеклассенумасинк**</span><span class="sxs-lookup"><span data-stu-id="144cb-110">**IWbemServices::CreateClassEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [<span data-ttu-id="144cb-111">**IWbemServices:: CreateInstanceEnum**</span><span class="sxs-lookup"><span data-stu-id="144cb-111">**IWbemServices::CreateInstanceEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [<span data-ttu-id="144cb-112">**IWbemServices:: Креатеинстанцеенумасинк**</span><span class="sxs-lookup"><span data-stu-id="144cb-112">**IWbemServices::CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [<span data-ttu-id="144cb-113">**IWbemServices:: ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="144cb-113">**IWbemServices::ExecQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [<span data-ttu-id="144cb-114">**IWbemServices:: Ексеккуерясинк**</span><span class="sxs-lookup"><span data-stu-id="144cb-114">**IWbemServices::ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [<span data-ttu-id="144cb-115">**IWbemServices:: GetObject**</span><span class="sxs-lookup"><span data-stu-id="144cb-115">**IWbemServices::GetObject**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [<span data-ttu-id="144cb-116">**IWbemServices:: Жетобжектасинк**</span><span class="sxs-lookup"><span data-stu-id="144cb-116">**IWbemServices::GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [<span data-ttu-id="144cb-117">**IWbemServices::P Уткласс**</span><span class="sxs-lookup"><span data-stu-id="144cb-117">**IWbemServices::PutClass**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [<span data-ttu-id="144cb-118">**IWbemServices::P Утклассасинк**</span><span class="sxs-lookup"><span data-stu-id="144cb-118">**IWbemServices::PutClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [<span data-ttu-id="144cb-119">**IWbemServices::P Утинстанце**</span><span class="sxs-lookup"><span data-stu-id="144cb-119">**IWbemServices::PutInstance**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [<span data-ttu-id="144cb-120">**IWbemServices::P Утинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="144cb-120">**IWbemServices::PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 




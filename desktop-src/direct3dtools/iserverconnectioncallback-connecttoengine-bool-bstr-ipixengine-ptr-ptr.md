---
description: Подключитесь к другому экземпляру удаленного модуля на локальном компьютере.
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исерверконнектионкаллбакк:: Коннекттоенгине'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140558"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span data-ttu-id="8e519-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>Метод Исерверконнектионкаллбакк:: Коннекттоенгине</span><span class="sxs-lookup"><span data-stu-id="8e519-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback::ConnectToEngine method</span></span>

<span data-ttu-id="8e519-104">Подключитесь к другому экземпляру удаленного модуля на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8e519-104">Connect to another instance of a remote engine on the local machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e519-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e519-105">Syntax</span></span>


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a><span data-ttu-id="8e519-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e519-106">Parameters</span></span>

<span data-ttu-id="8e519-107">*блегациконнектион* </span><span class="sxs-lookup"><span data-stu-id="8e519-107">*bLegacyConnection* </span></span>  
<span data-ttu-id="8e519-108">значение true, если ядро использует устаревшее значение; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="8e519-108">true if the engine uses is legacy, otherwise false.</span></span>

<span data-ttu-id="8e519-109">*рунаддресс* </span><span class="sxs-lookup"><span data-stu-id="8e519-109">*runAddress* </span></span>  
<span data-ttu-id="8e519-110">Строка COM, содержащая имя локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="8e519-110">A COM string containing the name of the local machine.</span></span>

<span data-ttu-id="8e519-111">*ппенгинекреатед* </span><span class="sxs-lookup"><span data-stu-id="8e519-111">*ppEngineCreated* </span></span>  
<span data-ttu-id="8e519-112">При возвращении — адрес экземпляра ядра.</span><span class="sxs-lookup"><span data-stu-id="8e519-112">On return, the address of the engine instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e519-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e519-113">Return value</span></span>

<span data-ttu-id="8e519-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8e519-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e519-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e519-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e519-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8e519-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8e519-117">Header</span><span class="sxs-lookup"><span data-stu-id="8e519-117">Header</span></span></p></td><td><span data-ttu-id="8e519-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="8e519-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8e519-119"><span id="see_also"></span> См. также</span><span class="sxs-lookup"><span data-stu-id="8e519-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8e519-120">**исерверконнектионкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="8e519-120">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 

---
description: Свойство Аутореконнект объекта Свбемрефрешер является логическим значением, указывающим, будет ли Обновитель автоматически повторно подключаться к удаленному поставщику, если соединение разорвано.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Свойство Свбемрефрешер. Аутореконнект (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351322"
---
# <a name="swbemrefresherautoreconnect-property"></a><span data-ttu-id="44e19-103">Свбемрефрешер. Аутореконнект, свойство</span><span class="sxs-lookup"><span data-stu-id="44e19-103">SWbemRefresher.AutoReconnect property</span></span>

<span data-ttu-id="44e19-104">Свойство **аутореконнект** объекта [**свбемрефрешер**](swbemrefresher.md) является логическим значением, указывающим, будет ли Обновитель автоматически повторно подключаться к удаленному поставщику, если соединение разорвано.</span><span class="sxs-lookup"><span data-stu-id="44e19-104">The **AutoReconnect** property of the [**SWbemRefresher**](swbemrefresher.md) object is a Boolean value that indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span>

<span data-ttu-id="44e19-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="44e19-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="44e19-106">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="44e19-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e19-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44e19-107">Syntax</span></span>


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a><span data-ttu-id="44e19-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="44e19-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="44e19-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44e19-109">Remarks</span></span>

<span data-ttu-id="44e19-110">Изменение этого свойства влияет только на объекты в обновитель, которые поддерживаются высокопроизводительным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="44e19-110">Modifying this property affects only objects in the refresher that are backed by a high-performance provider.</span></span> <span data-ttu-id="44e19-111">Если поставщик не является высокопроизводительным, установка свойства **аутореконнект** в **значение true** не оказывает никакого влияния, так как объект [**свбемрефрешер**](swbemrefresher.md) никогда не будет повторно подключаться.</span><span class="sxs-lookup"><span data-stu-id="44e19-111">If the provider is not a high-performance provider, then setting the **AutoReconnect** property to **TRUE** has no effect because the [**SWbemRefresher**](swbemrefresher.md) object never reconnects.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e19-112">Требования</span><span class="sxs-lookup"><span data-stu-id="44e19-112">Requirements</span></span>



| <span data-ttu-id="44e19-113">Требование</span><span class="sxs-lookup"><span data-stu-id="44e19-113">Requirement</span></span> | <span data-ttu-id="44e19-114">Значение</span><span class="sxs-lookup"><span data-stu-id="44e19-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44e19-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44e19-115">Minimum supported client</span></span><br/> | <span data-ttu-id="44e19-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44e19-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44e19-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44e19-117">Minimum supported server</span></span><br/> | <span data-ttu-id="44e19-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44e19-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44e19-119">Header</span><span class="sxs-lookup"><span data-stu-id="44e19-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e19-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="44e19-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="44e19-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="44e19-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="44e19-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="44e19-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="44e19-123">DLL</span><span class="sxs-lookup"><span data-stu-id="44e19-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44e19-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44e19-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="44e19-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="44e19-125">CLSID</span></span><br/>                    | <span data-ttu-id="44e19-126">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="44e19-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="44e19-127">IID</span><span class="sxs-lookup"><span data-stu-id="44e19-127">IID</span></span><br/>                      | <span data-ttu-id="44e19-128">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="44e19-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="44e19-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44e19-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e19-130">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="44e19-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 





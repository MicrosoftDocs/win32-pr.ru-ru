---
description: Метод Свбемрефрешер. Refresh обновляет все элементы, содержащиеся в объекте Свбемрефрешер. Объект Свбемрефрешер.
ms.assetid: 85a4777a-4be7-44f2-b7a6-e18b5e57f7af
ms.tgt_platform: multiple
title: Метод Свбемрефрешер. Refresh (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Refresh
- ISWbemRefresher.Refresh
- ISWbemRefresher.Refresh
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8b2522227041858770c7256d7d2520cc661948e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703459"
---
# <a name="swbemrefresherrefresh-method"></a><span data-ttu-id="b3a26-103">Свбемрефрешер. Refresh, метод</span><span class="sxs-lookup"><span data-stu-id="b3a26-103">SWbemRefresher.Refresh method</span></span>

<span data-ttu-id="b3a26-104">Метод **свбемрефрешер. Refresh** обновляет все элементы, содержащиеся в объекте [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="b3a26-104">The **SWbemRefresher.Refresh** method updates all the items that are contained in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="b3a26-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b3a26-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a26-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3a26-106">Syntax</span></span>


```VB
SWbemRefresher.Refresh( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b3a26-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3a26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a26-108">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="b3a26-108">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b3a26-109">Для флагов необходимо задать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="b3a26-109">Flags must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a26-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3a26-110">Return value</span></span>

<span data-ttu-id="b3a26-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b3a26-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a26-112">Требования</span><span class="sxs-lookup"><span data-stu-id="b3a26-112">Requirements</span></span>



| <span data-ttu-id="b3a26-113">Требование</span><span class="sxs-lookup"><span data-stu-id="b3a26-113">Requirement</span></span> | <span data-ttu-id="b3a26-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b3a26-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a26-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3a26-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a26-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3a26-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3a26-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3a26-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a26-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3a26-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3a26-119">Header</span><span class="sxs-lookup"><span data-stu-id="b3a26-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3a26-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a26-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3a26-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b3a26-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3a26-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b3a26-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b3a26-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b3a26-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3a26-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3a26-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b3a26-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="b3a26-125">CLSID</span></span><br/>                    | <span data-ttu-id="b3a26-126">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="b3a26-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="b3a26-127">IID</span><span class="sxs-lookup"><span data-stu-id="b3a26-127">IID</span></span><br/>                      | <span data-ttu-id="b3a26-128">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="b3a26-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="b3a26-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3a26-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a26-130">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="b3a26-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 





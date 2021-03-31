---
title: Имсрдппреферредредиректионинфо Усередиректионсервернаме, свойство
description: Возвращает или задает значение, указывающее, следует ли использовать имя сервера перенаправления.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Усередиректионсервернаме
- Службы удаленных рабочих столов свойства Усередиректионсервернаме, интерфейс Имсрдппреферредредиректионинфо
- Службы удаленных рабочих столов интерфейса Имсрдппреферредредиректионинфо, свойство Усередиректионсервернаме
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801720"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a><span data-ttu-id="69b02-106">Свойство Имсрдппреферредредиректионинфо:: Усередиректионсервернаме</span><span class="sxs-lookup"><span data-stu-id="69b02-106">IMsRdpPreferredRedirectionInfo::UseRedirectionServerName property</span></span>

<span data-ttu-id="69b02-107">Возвращает или задает значение, указывающее, следует ли использовать имя сервера перенаправления.</span><span class="sxs-lookup"><span data-stu-id="69b02-107">Gets and sets whether to use the redirection server name.</span></span>

<span data-ttu-id="69b02-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="69b02-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b02-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69b02-109">Syntax</span></span>


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a><span data-ttu-id="69b02-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="69b02-110">Property value</span></span>

<span data-ttu-id="69b02-111">Указывает, следует ли использовать имя сервера перенаправления.</span><span class="sxs-lookup"><span data-stu-id="69b02-111">Whether to use the redirection server name.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b02-112">Требования</span><span class="sxs-lookup"><span data-stu-id="69b02-112">Requirements</span></span>



| <span data-ttu-id="69b02-113">Требование</span><span class="sxs-lookup"><span data-stu-id="69b02-113">Requirement</span></span> | <span data-ttu-id="69b02-114">Значение</span><span class="sxs-lookup"><span data-stu-id="69b02-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69b02-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69b02-115">Minimum supported client</span></span><br/> | <span data-ttu-id="69b02-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="69b02-116">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="69b02-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69b02-117">Minimum supported server</span></span><br/> | <span data-ttu-id="69b02-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69b02-118">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="69b02-119">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="69b02-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="69b02-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69b02-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="69b02-121">DLL</span><span class="sxs-lookup"><span data-stu-id="69b02-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69b02-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69b02-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="69b02-123">IID</span><span class="sxs-lookup"><span data-stu-id="69b02-123">IID</span></span><br/>                      | <span data-ttu-id="69b02-124">IID \_ имсрдппреферредредиректионинфо определен как FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="69b02-124">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69b02-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69b02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b02-126">**имсрдппреферредредиректионинфо**</span><span class="sxs-lookup"><span data-stu-id="69b02-126">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 






---
description: Возвращает число поставщиков криптографических служб (CSP).
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'Свойство Искрденр:: Кспкаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348515"
---
# <a name="iscrdenrcspcount-property"></a><span data-ttu-id="ef5d7-103">Свойство Искрденр:: Кспкаунт</span><span class="sxs-lookup"><span data-stu-id="ef5d7-103">ISCrdEnr::CSPCount property</span></span>

<span data-ttu-id="ef5d7-104">Свойство **кспкаунт** Извлекает число [*поставщиков криптографических служб*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="ef5d7-104">The **CSPCount** property retrieves the number of [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

<span data-ttu-id="ef5d7-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ef5d7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef5d7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef5d7-106">Syntax</span></span>


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="ef5d7-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ef5d7-107">Property value</span></span>

<span data-ttu-id="ef5d7-108">Число CSP.</span><span class="sxs-lookup"><span data-stu-id="ef5d7-108">The number of CSPs.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef5d7-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ef5d7-109">Error codes</span></span>

<span data-ttu-id="ef5d7-110">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ef5d7-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="ef5d7-111">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ef5d7-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ef5d7-112">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="ef5d7-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef5d7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ef5d7-113">Requirements</span></span>



| <span data-ttu-id="ef5d7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ef5d7-114">Requirement</span></span> | <span data-ttu-id="ef5d7-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ef5d7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef5d7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef5d7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef5d7-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ef5d7-117">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ef5d7-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef5d7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef5d7-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ef5d7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef5d7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ef5d7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef5d7-121"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef5d7-121"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ef5d7-122">IID</span><span class="sxs-lookup"><span data-stu-id="ef5d7-122">IID</span></span><br/>                      | <span data-ttu-id="ef5d7-123">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ef5d7-123">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ef5d7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef5d7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef5d7-125">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="ef5d7-125">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ef5d7-126">**Искрденр:: CSPName**</span><span class="sxs-lookup"><span data-stu-id="ef5d7-126">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> <dt>

[<span data-ttu-id="ef5d7-127">**Искрденр:: Енумкспнаме**</span><span class="sxs-lookup"><span data-stu-id="ef5d7-127">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 

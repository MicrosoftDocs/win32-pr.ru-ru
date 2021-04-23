---
description: Задает или получает имя поставщика служб шифрования (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Свойство Искрденр:: CSPName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081438"
---
# <a name="iscrdenrcspname-property"></a><span data-ttu-id="c2ece-103">Свойство Искрденр:: CSPName</span><span class="sxs-lookup"><span data-stu-id="c2ece-103">ISCrdEnr::CSPName property</span></span>

<span data-ttu-id="c2ece-104">Свойство **CSPName** задает или получает имя [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="c2ece-104">The **CSPName** property sets or retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="c2ece-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c2ece-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ece-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2ece-106">Syntax</span></span>


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="c2ece-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c2ece-107">Property value</span></span>

<span data-ttu-id="c2ece-108">Имя CSP.</span><span class="sxs-lookup"><span data-stu-id="c2ece-108">The name of the CSP.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2ece-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c2ece-109">Error codes</span></span>

<span data-ttu-id="c2ece-110">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c2ece-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="c2ece-111">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c2ece-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="c2ece-112">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="c2ece-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ece-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2ece-113">Remarks</span></span>

<span data-ttu-id="c2ece-114">Задайте это свойство, чтобы указать имя CSP, используемого для управления регистрацией смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="c2ece-114">Set this property to specify the name of the CSP to use with the Smart Card Enrollment Control.</span></span> <span data-ttu-id="c2ece-115">Получите это свойство, чтобы получить имя указанного CSP.</span><span class="sxs-lookup"><span data-stu-id="c2ece-115">Get this property to retrieve the name of the specified CSP.</span></span> <span data-ttu-id="c2ece-116">Если значение для этого свойства не указано, свойство **CSPName** по умолчанию имеет имя, указанное в списке доступных CSP.</span><span class="sxs-lookup"><span data-stu-id="c2ece-116">If you do not specify a value for this property, the **CSPName** property defaults to the first name in the available list of CSPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ece-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c2ece-117">Requirements</span></span>



| <span data-ttu-id="c2ece-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c2ece-118">Requirement</span></span> | <span data-ttu-id="c2ece-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c2ece-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ece-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2ece-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ece-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c2ece-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c2ece-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2ece-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ece-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2ece-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2ece-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c2ece-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2ece-125"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2ece-125"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="c2ece-126">IID</span><span class="sxs-lookup"><span data-stu-id="c2ece-126">IID</span></span><br/>                      | <span data-ttu-id="c2ece-127">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="c2ece-127">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c2ece-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2ece-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ece-129">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="c2ece-129">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="c2ece-130">**Искрденр:: Кспкаунт**</span><span class="sxs-lookup"><span data-stu-id="c2ece-130">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="c2ece-131">**Искрденр:: Енумкспнаме**</span><span class="sxs-lookup"><span data-stu-id="c2ece-131">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 

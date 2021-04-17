---
description: Перечисляет имена доступных поставщиков служб шифрования (CSP).
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'Метод Искрденр:: Енумкспнаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546682"
---
# <a name="iscrdenrenumcspname-method"></a><span data-ttu-id="eb8a4-103">Метод Искрденр:: Енумкспнаме</span><span class="sxs-lookup"><span data-stu-id="eb8a4-103">ISCrdEnr::enumCSPName method</span></span>

<span data-ttu-id="eb8a4-104">Метод **енумкспнаме** перечисляет имена доступных [*поставщиков служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="eb8a4-104">The **enumCSPName** method enumerates the name of the available [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb8a4-105">Syntax</span></span>


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a><span data-ttu-id="eb8a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb8a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb8a4-107">*двиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb8a4-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb8a4-108">Отсчитываемый от нуля индекс последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="eb8a4-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="eb8a4-109">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eb8a4-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb8a4-110">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="eb8a4-110">Reserved for future use.</span></span> <span data-ttu-id="eb8a4-111">Присвойте этому параметру значение 0.</span><span class="sxs-lookup"><span data-stu-id="eb8a4-111">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="eb8a4-112">*пбстркспнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="eb8a4-112">*pbstrCSPName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb8a4-113">Указатель на строку, которая возвращает имя перечисленного CSP.</span><span class="sxs-lookup"><span data-stu-id="eb8a4-113">A pointer to a string that returns the name of the enumerated CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb8a4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb8a4-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="eb8a4-115">C++</span><span class="sxs-lookup"><span data-stu-id="eb8a4-115">C++</span></span>

<span data-ttu-id="eb8a4-116">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="eb8a4-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="eb8a4-117">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="eb8a4-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="eb8a4-118">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="eb8a4-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="eb8a4-119">VB</span><span class="sxs-lookup"><span data-stu-id="eb8a4-119">VB</span></span>

<span data-ttu-id="eb8a4-120">Строка, представляющая имя перечисленного CSP.</span><span class="sxs-lookup"><span data-stu-id="eb8a4-120">A string that represents the name of the enumerated CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb8a4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="eb8a4-121">Requirements</span></span>



| <span data-ttu-id="eb8a4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="eb8a4-122">Requirement</span></span> | <span data-ttu-id="eb8a4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="eb8a4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8a4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb8a4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8a4-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="eb8a4-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="eb8a4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb8a4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8a4-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb8a4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb8a4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="eb8a4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb8a4-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb8a4-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb8a4-130">IID</span><span class="sxs-lookup"><span data-stu-id="eb8a4-130">IID</span></span><br/>                      | <span data-ttu-id="eb8a4-131">IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="eb8a4-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="eb8a4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb8a4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8a4-133">**искрденр**</span><span class="sxs-lookup"><span data-stu-id="eb8a4-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="eb8a4-134">**Искрденр:: Кспкаунт**</span><span class="sxs-lookup"><span data-stu-id="eb8a4-134">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="eb8a4-135">**Искрденр:: CSPName**</span><span class="sxs-lookup"><span data-stu-id="eb8a4-135">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> </dl>

 

 

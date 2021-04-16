---
description: Сравнивает два маркера доступа и определяет, эквивалентны ли они в отношении вызова функции AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Функция Нткомпаретокенс (Нтсеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650676"
---
# <a name="ntcomparetokens-function"></a><span data-ttu-id="4b328-103">Функция Нткомпаретокенс</span><span class="sxs-lookup"><span data-stu-id="4b328-103">NtCompareTokens function</span></span>

<span data-ttu-id="4b328-104">Функция **нткомпаретокенс** сравнивает два [*маркера доступа*](/windows/desktop/SecGloss/a-gly) и определяет, эквивалентны ли они в отношении вызова функции [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .</span><span class="sxs-lookup"><span data-stu-id="4b328-104">The **NtCompareTokens** function compares two [*access tokens*](/windows/desktop/SecGloss/a-gly) and determines whether they are equivalent with respect to a call to the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b328-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b328-105">Syntax</span></span>


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a><span data-ttu-id="4b328-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b328-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b328-107">*Фирсттокенхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b328-107">*FirstTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b328-108">Маркер первого маркера доступа для сравнения.</span><span class="sxs-lookup"><span data-stu-id="4b328-108">A handle to the first access token to compare.</span></span> <span data-ttu-id="4b328-109">Токен должен быть открыт для доступа **к \_ запросам маркеров** .</span><span class="sxs-lookup"><span data-stu-id="4b328-109">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="4b328-110">*Секондтокенхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b328-110">*SecondTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b328-111">Маркер второго маркера доступа для сравнения.</span><span class="sxs-lookup"><span data-stu-id="4b328-111">A handle to the second access token to compare.</span></span> <span data-ttu-id="4b328-112">Токен должен быть открыт для доступа **к \_ запросам маркеров** .</span><span class="sxs-lookup"><span data-stu-id="4b328-112">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="4b328-113">*Равно* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4b328-113">*Equal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b328-114">Указатель на переменную, которая получает значение, указывающее, эквивалентны ли маркеры, представленные параметрами *фирсттокенхандле* и *секондтокенхандле* .</span><span class="sxs-lookup"><span data-stu-id="4b328-114">A pointer to a variable that receives a value that indicates whether the tokens represented by the *FirstTokenHandle* and *SecondTokenHandle* parameters are equivalent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b328-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b328-115">Return value</span></span>

<span data-ttu-id="4b328-116">Если функция завершается успешно, функция возвращает состояние \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4b328-116">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="4b328-117">Если функция завершается ошибкой, возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="4b328-117">If the function fails, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b328-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b328-118">Remarks</span></span>

<span data-ttu-id="4b328-119">Два маркера управления доступом считаются эквивалентными, если выполняются все перечисленные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="4b328-119">Two access control tokens are considered to be equivalent if all of the following conditions are true:</span></span>

-   <span data-ttu-id="4b328-120">Каждый [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID), присутствующий в обоих маркерах, также имеется в другом токене.</span><span class="sxs-lookup"><span data-stu-id="4b328-120">Every [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) that is present in either token is also present in the other token.</span></span>
-   <span data-ttu-id="4b328-121">Ни один из маркеров, ни оба не ограничены.</span><span class="sxs-lookup"><span data-stu-id="4b328-121">Neither or both of the tokens are restricted.</span></span>
-   <span data-ttu-id="4b328-122">Если оба токена ограничены, каждый идентификатор безопасности, ограниченный в одном маркере, также ограничен в другом токене.</span><span class="sxs-lookup"><span data-stu-id="4b328-122">If both tokens are restricted, every SID that is restricted in one token is also restricted in the other token.</span></span>
-   <span data-ttu-id="4b328-123">Все привилегии, имеющиеся в обоих маркерах, также существуют в другом маркере.</span><span class="sxs-lookup"><span data-stu-id="4b328-123">Every privilege present in either token is also present in the other token.</span></span>

<span data-ttu-id="4b328-124">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4b328-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b328-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4b328-125">Requirements</span></span>



| <span data-ttu-id="4b328-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4b328-126">Requirement</span></span> | <span data-ttu-id="4b328-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4b328-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4b328-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b328-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b328-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b328-129">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4b328-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b328-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b328-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b328-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4b328-132">Header</span><span class="sxs-lookup"><span data-stu-id="4b328-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b328-133"><dt>Нтсеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b328-133"><dt>Ntseapi.h</dt></span></span> </dl> |
| <span data-ttu-id="4b328-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4b328-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b328-135"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b328-135"><dt>Ntdll.dll</dt></span></span> </dl> |



 


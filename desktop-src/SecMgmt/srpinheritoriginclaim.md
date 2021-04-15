---
description: Эта функция принимает начальный атрибут, если он существует из исходного маркера, и устанавливает их на дубликате наследуемого маркера и возвращает дублирующийся токен.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: Функция Српинхериторигинклаим
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682580"
---
# <a name="srpinheritoriginclaim-function"></a><span data-ttu-id="b5f71-103">Функция Српинхериторигинклаим</span><span class="sxs-lookup"><span data-stu-id="b5f71-103">srpInheritOriginClaim function</span></span>

<span data-ttu-id="b5f71-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b5f71-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b5f71-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b5f71-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b5f71-106">Эта функция принимает начальный атрибут, если он существует из исходного маркера, и устанавливает их на дубликате наследуемого маркера и возвращает дублирующийся токен.</span><span class="sxs-lookup"><span data-stu-id="b5f71-106">This function takes the origin attribute if present from the origin token and sets them on a duplicate of the inheriting token, and returns the duplicate token.</span></span> <span data-ttu-id="b5f71-107">Затем вызывающий объект может олицетворять возвращенный токен.</span><span class="sxs-lookup"><span data-stu-id="b5f71-107">The caller can then impersonate the returned token.</span></span> <span data-ttu-id="b5f71-108">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="b5f71-108">This function has no associated import library.</span></span> <span data-ttu-id="b5f71-109">Для динамической привязки к srpapi.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="b5f71-109">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to srpapi.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f71-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5f71-110">Syntax</span></span>


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a><span data-ttu-id="b5f71-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5f71-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f71-112">*Оригинтокен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5f71-112">*OriginToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f71-113">Маркер, который дублируется и получает наследуемый атрибут источника.</span><span class="sxs-lookup"><span data-stu-id="b5f71-113">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="b5f71-114">Этот маркер должен быть открыт с \_ правом доступа к маркеру "дублировать".</span><span class="sxs-lookup"><span data-stu-id="b5f71-114">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span>

</dd> <dt>

<span data-ttu-id="b5f71-115">*Инхеритингтокен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b5f71-115">*InheritingToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f71-116">Маркер, который дублируется и получает наследуемый атрибут источника.</span><span class="sxs-lookup"><span data-stu-id="b5f71-116">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="b5f71-117">Этот маркер должен быть открыт с \_ правом доступа к маркеру "дублировать".</span><span class="sxs-lookup"><span data-stu-id="b5f71-117">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span> 

</dd> <dt>

<span data-ttu-id="b5f71-118">*ресулттокен*</span><span class="sxs-lookup"><span data-stu-id="b5f71-118">*ResultToken*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f71-119">При успешном выполнении получает дубликат токена.</span><span class="sxs-lookup"><span data-stu-id="b5f71-119">On success, receives the duplicated token.</span></span> <span data-ttu-id="b5f71-120">Вызывающий объект может олицетворять его для выполнения операций с унаследованным атрибутом Origin.</span><span class="sxs-lookup"><span data-stu-id="b5f71-120">The caller can impersonate it to perform operations with the inherited origin attribute.</span></span> <span data-ttu-id="b5f71-121">Вызывающий объект принимает владение этим маркером и должен закрыть его.</span><span class="sxs-lookup"><span data-stu-id="b5f71-121">The caller takes ownership of this handle and must close it.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f71-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5f71-122">Return value</span></span>

<span data-ttu-id="b5f71-123">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="b5f71-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5f71-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5f71-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f71-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b5f71-125">Requirements</span></span>



| <span data-ttu-id="b5f71-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b5f71-126">Requirement</span></span> | <span data-ttu-id="b5f71-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b5f71-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f71-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5f71-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f71-129">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b5f71-129">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b5f71-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5f71-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f71-131">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="b5f71-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5f71-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b5f71-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5f71-133"><dt>Srpapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5f71-133"><dt>Srpapi.dll</dt></span></span> </dl> |



 


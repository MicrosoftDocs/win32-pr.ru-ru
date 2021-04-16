---
description: Возвращает строку, содержащую идентификатор самонастраивающийся для устройства планшета.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'Метод Итаблет:: Жетплугандплайид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719564"
---
# <a name="itabletgetplugandplayid-method"></a><span data-ttu-id="0cdb8-103">Метод Итаблет:: Жетплугандплайид</span><span class="sxs-lookup"><span data-stu-id="0cdb8-103">ITablet::GetPlugAndPlayId method</span></span>

<span data-ttu-id="0cdb8-104">Возвращает строку, содержащую идентификатор самонастраивающийся для устройства планшета.</span><span class="sxs-lookup"><span data-stu-id="0cdb8-104">Returns a string containing the Plug and Play ID for the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cdb8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cdb8-105">Syntax</span></span>


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a><span data-ttu-id="0cdb8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cdb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cdb8-107">*ппвсзппид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0cdb8-107">*ppwszPPId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cdb8-108">Указатель на строку, содержащую идентификатор самонастраивающийся для устройства планшета.</span><span class="sxs-lookup"><span data-stu-id="0cdb8-108">Pointer to a string containing the Plug and Play ID for the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cdb8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cdb8-109">Return value</span></span>

<span data-ttu-id="0cdb8-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0cdb8-110">This method can return one of these values.</span></span>



| <span data-ttu-id="0cdb8-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0cdb8-111">Return code</span></span>                                                                            | <span data-ttu-id="0cdb8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0cdb8-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0cdb8-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb8-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0cdb8-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="0cdb8-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="0cdb8-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb8-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0cdb8-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0cdb8-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0cdb8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0cdb8-117">Remarks</span></span>

<span data-ttu-id="0cdb8-118">Он отвечает за освобождение памяти, возвращаемой этим методом, с помощью [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="0cdb8-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cdb8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0cdb8-119">Requirements</span></span>



| <span data-ttu-id="0cdb8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0cdb8-120">Requirement</span></span> | <span data-ttu-id="0cdb8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0cdb8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cdb8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cdb8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0cdb8-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0cdb8-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0cdb8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cdb8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0cdb8-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0cdb8-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0cdb8-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0cdb8-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cdb8-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb8-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cdb8-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cdb8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cdb8-129">**Интерфейс Итаблет**</span><span class="sxs-lookup"><span data-stu-id="0cdb8-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 


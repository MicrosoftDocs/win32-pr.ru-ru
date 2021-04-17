---
description: Возвращает значение, указывающее, поддерживает ли указанная система ключей указанный тип носителя.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'Метод Имфмедиаенгинеклассфакторекс:: Истипесуппортед'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693818"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a><span data-ttu-id="35ed2-103">Метод Имфмедиаенгинеклассфакторекс:: Истипесуппортед</span><span class="sxs-lookup"><span data-stu-id="35ed2-103">IMFMediaEngineClassFactoryEx::IsTypeSupported method</span></span>

<span data-ttu-id="35ed2-104">Возвращает значение, указывающее, поддерживает ли указанная система ключей указанный тип носителя.</span><span class="sxs-lookup"><span data-stu-id="35ed2-104">Gets a value that indicates if the specified key system supports the specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ed2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35ed2-105">Syntax</span></span>


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a><span data-ttu-id="35ed2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35ed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ed2-107">*type*</span><span class="sxs-lookup"><span data-stu-id="35ed2-107">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="35ed2-108">Тип MIME для проверки поддержки.</span><span class="sxs-lookup"><span data-stu-id="35ed2-108">The MIME type to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="35ed2-109">*кэйсистем*</span><span class="sxs-lookup"><span data-stu-id="35ed2-109">*keySystem*</span></span> 
</dt> <dd>

<span data-ttu-id="35ed2-110">Основная система для проверки поддержки.</span><span class="sxs-lookup"><span data-stu-id="35ed2-110">The key system to check support for.</span></span>

</dd> <dt>

<span data-ttu-id="35ed2-111">*isSupported*</span><span class="sxs-lookup"><span data-stu-id="35ed2-111">*isSupported*</span></span> 
</dt> <dd>

<span data-ttu-id="35ed2-112">**значение true** , если тип поддерживается *кэйсистем*; в противном случае — **значение false.**</span><span class="sxs-lookup"><span data-stu-id="35ed2-112">**true** if type is supported by *keySystem*; otherwise, **false.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ed2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35ed2-113">Return value</span></span>

<span data-ttu-id="35ed2-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="35ed2-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35ed2-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35ed2-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ed2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="35ed2-116">Requirements</span></span>



| <span data-ttu-id="35ed2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="35ed2-117">Requirement</span></span> | <span data-ttu-id="35ed2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="35ed2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ed2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35ed2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35ed2-120">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="35ed2-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="35ed2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35ed2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35ed2-122">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35ed2-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="35ed2-123">IDL</span><span class="sxs-lookup"><span data-stu-id="35ed2-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35ed2-124"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35ed2-124"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ed2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35ed2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ed2-126">**имфмедиаенгинеклассфакторекс**</span><span class="sxs-lookup"><span data-stu-id="35ed2-126">**IMFMediaEngineClassFactoryEx**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 





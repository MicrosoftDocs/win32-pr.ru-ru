---
description: Передает значение ключа со всеми связанными данными, необходимыми модулю расшифровки содержимого для заданной ключевой системы.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'Метод Имфмедиакэйсессион:: Update'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664831"
---
# <a name="imfmediakeysessionupdate-method"></a><span data-ttu-id="e3352-103">Метод Имфмедиакэйсессион:: Update</span><span class="sxs-lookup"><span data-stu-id="e3352-103">IMFMediaKeySession::Update method</span></span>

<span data-ttu-id="e3352-104">Передает значение ключа со всеми связанными данными, необходимыми модулю расшифровки содержимого для заданной ключевой системы.</span><span class="sxs-lookup"><span data-stu-id="e3352-104">Passes in a key value with any associated data required by the Content Decryption Module for the given key system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3352-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3352-105">Syntax</span></span>


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a><span data-ttu-id="e3352-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3352-107">*key*</span><span class="sxs-lookup"><span data-stu-id="e3352-107">*key*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="e3352-108">*CB*</span><span class="sxs-lookup"><span data-stu-id="e3352-108">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="e3352-109">Число в байтах *ключа*.</span><span class="sxs-lookup"><span data-stu-id="e3352-109">The count in bytes of *key*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3352-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3352-110">Return value</span></span>

<span data-ttu-id="e3352-111">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="e3352-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3352-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3352-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3352-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e3352-113">Requirements</span></span>



| <span data-ttu-id="e3352-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e3352-114">Requirement</span></span> | <span data-ttu-id="e3352-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e3352-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3352-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3352-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3352-117">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e3352-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e3352-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3352-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3352-119">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3352-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e3352-120">IDL</span><span class="sxs-lookup"><span data-stu-id="e3352-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3352-121"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3352-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3352-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3352-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3352-123">**имфмедиакэйсессион**</span><span class="sxs-lookup"><span data-stu-id="e3352-123">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 





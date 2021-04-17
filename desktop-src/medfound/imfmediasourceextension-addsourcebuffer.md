---
description: Добавляет Имфсаурцебуффер в коллекцию буферов, связанных с Имфмедиасаурцеекстенсион.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'Метод Имфмедиасаурцеекстенсион:: Аддсаурцебуффер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703457"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a><span data-ttu-id="be315-103">Метод Имфмедиасаурцеекстенсион:: Аддсаурцебуффер</span><span class="sxs-lookup"><span data-stu-id="be315-103">IMFMediaSourceExtension::AddSourceBuffer method</span></span>

<span data-ttu-id="be315-104">Добавляет [**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) в коллекцию буферов, связанных с [**имфмедиасаурцеекстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span><span class="sxs-lookup"><span data-stu-id="be315-104">Adds a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) to the collection of buffers associated with the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span></span>

## <a name="syntax"></a><span data-ttu-id="be315-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be315-105">Syntax</span></span>


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="be315-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be315-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be315-107">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be315-107">*type* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="be315-108">*пнотифи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be315-108">*pNotify* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="be315-109">*ппсаурцебуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be315-109">*ppSourceBuffer* \[out\]</span></span>
<span data-ttu-id="be315-110"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="be315-110"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="be315-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be315-111">Return value</span></span>

<span data-ttu-id="be315-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="be315-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be315-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be315-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="be315-114">Требования</span><span class="sxs-lookup"><span data-stu-id="be315-114">Requirements</span></span>



| <span data-ttu-id="be315-115">Требование</span><span class="sxs-lookup"><span data-stu-id="be315-115">Requirement</span></span> | <span data-ttu-id="be315-116">Значение</span><span class="sxs-lookup"><span data-stu-id="be315-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="be315-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be315-117">Minimum supported client</span></span><br/> | <span data-ttu-id="be315-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be315-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be315-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be315-119">Minimum supported server</span></span><br/> | <span data-ttu-id="be315-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="be315-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="be315-121">IDL</span><span class="sxs-lookup"><span data-stu-id="be315-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be315-122"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be315-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be315-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be315-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be315-124">**имфмедиасаурцеекстенсион**</span><span class="sxs-lookup"><span data-stu-id="be315-124">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





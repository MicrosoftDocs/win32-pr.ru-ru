---
description: Удаляет указанный исходный буфер из коллекции исходных буферов, управляемых объектом Имфмедиасаурцеекстенсион.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'Метод Имфмедиасаурцеекстенсион:: Ремовесаурцебуффер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351515"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a><span data-ttu-id="25c4d-103">Метод Имфмедиасаурцеекстенсион:: Ремовесаурцебуффер</span><span class="sxs-lookup"><span data-stu-id="25c4d-103">IMFMediaSourceExtension::RemoveSourceBuffer method</span></span>

<span data-ttu-id="25c4d-104">Удаляет указанный исходный буфер из коллекции исходных буферов, управляемых объектом [**имфмедиасаурцеекстенсион**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) .</span><span class="sxs-lookup"><span data-stu-id="25c4d-104">Removes the specified source buffer from the collection of source buffers managed by the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25c4d-105">Syntax</span></span>


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="25c4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25c4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c4d-107">*псаурцебуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25c4d-107">*pSourceBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c4d-108">Буфер для удаления.</span><span class="sxs-lookup"><span data-stu-id="25c4d-108">The buffer to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c4d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25c4d-109">Return value</span></span>

<span data-ttu-id="25c4d-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="25c4d-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="25c4d-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25c4d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c4d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="25c4d-112">Requirements</span></span>



| <span data-ttu-id="25c4d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="25c4d-113">Requirement</span></span> | <span data-ttu-id="25c4d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="25c4d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="25c4d-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25c4d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="25c4d-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25c4d-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="25c4d-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25c4d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="25c4d-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="25c4d-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="25c4d-119">IDL</span><span class="sxs-lookup"><span data-stu-id="25c4d-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25c4d-120"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25c4d-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c4d-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25c4d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c4d-122">**имфмедиасаурцеекстенсион**</span><span class="sxs-lookup"><span data-stu-id="25c4d-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





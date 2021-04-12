---
description: Добавляет указанный сегмент мультимедиа в Имфсаурцебуффер.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: 'Метод Имфсаурцебуффер:: Append'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263369"
---
# <a name="imfsourcebufferappend-method"></a><span data-ttu-id="0eab5-103">Метод Имфсаурцебуффер:: Append</span><span class="sxs-lookup"><span data-stu-id="0eab5-103">IMFSourceBuffer::Append method</span></span>

<span data-ttu-id="0eab5-104">Добавляет указанный сегмент мультимедиа в [**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="0eab5-104">Appends the specified media segment to the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="0eab5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0eab5-105">Syntax</span></span>


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a><span data-ttu-id="0eab5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0eab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eab5-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0eab5-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eab5-108">Добавляемые данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0eab5-108">The media data to append.</span></span>

</dd> <dt>

<span data-ttu-id="0eab5-109">*Len* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0eab5-109">*len* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eab5-110">Длина данных мультимедиа, хранящихся в *pData*.</span><span class="sxs-lookup"><span data-stu-id="0eab5-110">The length of the media data stored in *pData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eab5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0eab5-111">Return value</span></span>

<span data-ttu-id="0eab5-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0eab5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0eab5-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0eab5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eab5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0eab5-114">Requirements</span></span>



| <span data-ttu-id="0eab5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0eab5-115">Requirement</span></span> | <span data-ttu-id="0eab5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0eab5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eab5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0eab5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0eab5-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0eab5-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0eab5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0eab5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0eab5-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0eab5-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0eab5-121">IDL</span><span class="sxs-lookup"><span data-stu-id="0eab5-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0eab5-122"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0eab5-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eab5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0eab5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eab5-124">**имфсаурцебуффер**</span><span class="sxs-lookup"><span data-stu-id="0eab5-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 





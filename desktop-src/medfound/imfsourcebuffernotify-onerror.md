---
description: Используется для указания на то, что в исходном буфере произошла ошибка.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'Метод Имфсаурцебуффернотифи:: OnError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701711"
---
# <a name="imfsourcebuffernotifyonerror-method"></a><span data-ttu-id="fb673-103">Метод Имфсаурцебуффернотифи:: OnError</span><span class="sxs-lookup"><span data-stu-id="fb673-103">IMFSourceBufferNotify::OnError method</span></span>

<span data-ttu-id="fb673-104">Используется для указания на то, что в исходном буфере произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="fb673-104">Used to indicate that an error has occurred with the source buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb673-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb673-105">Syntax</span></span>


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="fb673-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb673-107">*HR* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb673-107">*hr* \[in\]</span></span>
<span data-ttu-id="fb673-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fb673-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="fb673-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb673-109">Return value</span></span>

<span data-ttu-id="fb673-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fb673-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb673-111">Требования</span><span class="sxs-lookup"><span data-stu-id="fb673-111">Requirements</span></span>



| <span data-ttu-id="fb673-112">Требование</span><span class="sxs-lookup"><span data-stu-id="fb673-112">Requirement</span></span> | <span data-ttu-id="fb673-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fb673-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb673-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb673-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fb673-115">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fb673-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb673-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb673-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fb673-117">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb673-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fb673-118">IDL</span><span class="sxs-lookup"><span data-stu-id="fb673-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb673-119"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb673-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb673-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb673-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb673-121">**имфсаурцебуффернотифи**</span><span class="sxs-lookup"><span data-stu-id="fb673-121">**IMFSourceBufferNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 





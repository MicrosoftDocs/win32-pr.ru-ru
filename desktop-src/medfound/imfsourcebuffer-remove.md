---
description: Удаляет сегменты носителя, определенные в указанном диапазоне времени, из Имфсаурцебуффер.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'Метод Имфсаурцебуффер:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: d82660d08efe651b321672b6ccd0cb475875beee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711343"
---
# <a name="imfsourcebufferremove-method"></a><span data-ttu-id="a2afc-103">Метод Имфсаурцебуффер:: Remove</span><span class="sxs-lookup"><span data-stu-id="a2afc-103">IMFSourceBuffer::Remove method</span></span>

<span data-ttu-id="a2afc-104">Удаляет сегменты носителя, определенные в указанном диапазоне времени, из [**имфсаурцебуффер**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="a2afc-104">Removes the media segments defined by the specified time range from the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2afc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2afc-105">Syntax</span></span>


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a><span data-ttu-id="a2afc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2afc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2afc-107">*Запуск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2afc-107">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2afc-108">Начало диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="a2afc-108">The start of the time range.</span></span>

</dd> <dt>

<span data-ttu-id="a2afc-109">*конец* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2afc-109">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2afc-110">Конец диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="a2afc-110">The end of the time range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2afc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2afc-111">Return value</span></span>

<span data-ttu-id="a2afc-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a2afc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a2afc-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2afc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2afc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a2afc-114">Requirements</span></span>



| <span data-ttu-id="a2afc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a2afc-115">Requirement</span></span> | <span data-ttu-id="a2afc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2afc-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2afc-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2afc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2afc-118">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2afc-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2afc-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2afc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2afc-120">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2afc-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a2afc-121">IDL</span><span class="sxs-lookup"><span data-stu-id="a2afc-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2afc-122"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2afc-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2afc-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2afc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2afc-124">**имфсаурцебуффер**</span><span class="sxs-lookup"><span data-stu-id="a2afc-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 





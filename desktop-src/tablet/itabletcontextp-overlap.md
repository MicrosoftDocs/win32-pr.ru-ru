---
description: Перемещает контекст планшета на передний или задний план входной очереди.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'Метод Итаблетконтекстп:: перекрыт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712624"
---
# <a name="itabletcontextpoverlap-method"></a><span data-ttu-id="e0f7e-103">Метод Итаблетконтекстп:: перекрыт</span><span class="sxs-lookup"><span data-stu-id="e0f7e-103">ITabletContextP::Overlap method</span></span>

<span data-ttu-id="e0f7e-104">Перемещает контекст планшета на передний или задний план входной очереди.</span><span class="sxs-lookup"><span data-stu-id="e0f7e-104">Moves a tablet context to the front or back of the input queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0f7e-105">Syntax</span></span>


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a><span data-ttu-id="e0f7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0f7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f7e-107">*бтоп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0f7e-107">*bTop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f7e-108">Указывает, следует ли перемещать контекст планшета в верхнюю или нижнюю часть входной очереди.</span><span class="sxs-lookup"><span data-stu-id="e0f7e-108">Indicates if the tablet context should be moved to the top or bottom of the input queue.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7e-109">*пдвтЦид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e0f7e-109">*pdwtcid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f7e-110">Идентификатор контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="e0f7e-110">The tablet context identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f7e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0f7e-111">Return value</span></span>

<span data-ttu-id="e0f7e-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e0f7e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e0f7e-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e0f7e-113">Return code</span></span>                                                                            | <span data-ttu-id="e0f7e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e0f7e-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e0f7e-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f7e-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e0f7e-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="e0f7e-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e0f7e-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0f7e-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e0f7e-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e0f7e-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e0f7e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e0f7e-119">Requirements</span></span>



| <span data-ttu-id="e0f7e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e0f7e-120">Requirement</span></span> | <span data-ttu-id="e0f7e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e0f7e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0f7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f7e-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e0f7e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e0f7e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0f7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f7e-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e0f7e-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e0f7e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e0f7e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0f7e-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0f7e-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f7e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0f7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f7e-129">**Интерфейс Итаблетконтекстп**</span><span class="sxs-lookup"><span data-stu-id="e0f7e-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 





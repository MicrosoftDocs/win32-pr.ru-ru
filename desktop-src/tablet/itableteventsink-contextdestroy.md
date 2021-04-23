---
description: Происходит при уничтожении контекста планшета.
ms.assetid: 805289d8-267e-488b-8092-6b07b37dd6d4
title: 'Метод Итаблетевентсинк:: Контекстдестрой'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.ContextDestroy
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c9b5d78d4ce4032c1a7a2082fb749afc5a39949a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546735"
---
# <a name="itableteventsinkcontextdestroy-method"></a><span data-ttu-id="776c9-103">Метод Итаблетевентсинк:: Контекстдестрой</span><span class="sxs-lookup"><span data-stu-id="776c9-103">ITabletEventSink::ContextDestroy method</span></span>

<span data-ttu-id="776c9-104">Происходит при уничтожении контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="776c9-104">Occurs when a tablet context is being destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="776c9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="776c9-105">Syntax</span></span>


```C++
HRESULT ContextDestroy(
  [in] TABLET_CONTEXT_ID tcid
);
```



## <a name="parameters"></a><span data-ttu-id="776c9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="776c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="776c9-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="776c9-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="776c9-108">Идентификатор удаляемого контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="776c9-108">The identifier of the tablet context being destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="776c9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="776c9-109">Return value</span></span>

<span data-ttu-id="776c9-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="776c9-110">This method can return one of these values.</span></span>



| <span data-ttu-id="776c9-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="776c9-111">Return code</span></span>                                                                            | <span data-ttu-id="776c9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="776c9-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="776c9-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="776c9-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="776c9-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="776c9-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="776c9-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="776c9-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="776c9-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="776c9-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="776c9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="776c9-117">Requirements</span></span>



| <span data-ttu-id="776c9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="776c9-118">Requirement</span></span> | <span data-ttu-id="776c9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="776c9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="776c9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="776c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="776c9-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="776c9-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="776c9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="776c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="776c9-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="776c9-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="776c9-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="776c9-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="776c9-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="776c9-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="776c9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="776c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776c9-127">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="776c9-127">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 





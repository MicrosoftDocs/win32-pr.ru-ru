---
description: Содержит сведения, используемые при создании контекста планшета.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Структура TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999615"
---
# <a name="tablet_context_settings-structure"></a><span data-ttu-id="569cc-103">\_Структура параметров контекста планшета \_</span><span class="sxs-lookup"><span data-stu-id="569cc-103">TABLET\_CONTEXT\_SETTINGS structure</span></span>

<span data-ttu-id="569cc-104">Содержит сведения, используемые при создании контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="569cc-104">Contains information used in creating a tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="569cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="569cc-105">Syntax</span></span>


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a><span data-ttu-id="569cc-106">Члены</span><span class="sxs-lookup"><span data-stu-id="569cc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="569cc-107">**кпктпропс**</span><span class="sxs-lookup"><span data-stu-id="569cc-107">**cPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-108">Число свойств в пакете.</span><span class="sxs-lookup"><span data-stu-id="569cc-108">The number of properties in a packet.</span></span>

</dd> <dt>

<span data-ttu-id="569cc-109">**пгуидпктпропс**</span><span class="sxs-lookup"><span data-stu-id="569cc-109">**pguidPktProps**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-110">Уникальные идентификаторы для свойств пакета.</span><span class="sxs-lookup"><span data-stu-id="569cc-110">Unique identifiers for the packet properties.</span></span>

</dd> <dt>

<span data-ttu-id="569cc-111">**кпктбтнс**</span><span class="sxs-lookup"><span data-stu-id="569cc-111">**cPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-112">Число кнопок.</span><span class="sxs-lookup"><span data-stu-id="569cc-112">The number of buttons.</span></span>

</dd> <dt>

<span data-ttu-id="569cc-113">**пгуидпктбтнс**</span><span class="sxs-lookup"><span data-stu-id="569cc-113">**pguidPktBtns**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-114">Уникальные идентификаторы для кнопок.</span><span class="sxs-lookup"><span data-stu-id="569cc-114">Unique identifiers for the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="569cc-115">**пдвбтнднмаск**</span><span class="sxs-lookup"><span data-stu-id="569cc-115">**pdwBtnDnMask**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-116">Маска кнопки "вниз".</span><span class="sxs-lookup"><span data-stu-id="569cc-116">The button down mask.</span></span>

</dd> <dt>

<span data-ttu-id="569cc-117">**пдвбтнупмаск**</span><span class="sxs-lookup"><span data-stu-id="569cc-117">**pdwBtnUpMask**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-118">Кнопка "вверх".</span><span class="sxs-lookup"><span data-stu-id="569cc-118">The button up mask.</span></span>

</dd> <dt>

<span data-ttu-id="569cc-119">**лксмаргин**</span><span class="sxs-lookup"><span data-stu-id="569cc-119">**lXMargin**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-120">Поле направления по оси X.</span><span class="sxs-lookup"><span data-stu-id="569cc-120">The X direction margin.</span></span>

</dd> <dt>

<span data-ttu-id="569cc-121">**лимаргин**</span><span class="sxs-lookup"><span data-stu-id="569cc-121">**lYMargin**</span></span>
</dt> <dd>

<span data-ttu-id="569cc-122">Поле направления по оси Y.</span><span class="sxs-lookup"><span data-stu-id="569cc-122">The Y direction margin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="569cc-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="569cc-123">Remarks</span></span>

<span data-ttu-id="569cc-124">Как правило, приложение получает значения по умолчанию из [**метода итаблет:: жетдефаултконтекстсеттингс**](itablet-getdefaultcontextsettings.md), изменяет значения в соответствии с их потребностями, а затем передает измененную структуру параметров в [**метод Итаблет:: CreateContext**](itablet-createcontext.md).</span><span class="sxs-lookup"><span data-stu-id="569cc-124">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the [**ITablet::CreateContext Method**](itablet-createcontext.md).</span></span>

<span data-ttu-id="569cc-125">Эта структура определяет, какие события будут получены приложением, как они будут обработаны и как они будут переданы в приложение или в саму Windows.</span><span class="sxs-lookup"><span data-stu-id="569cc-125">This structure determines what events an application will get, how they will be processed, and how they will be delivered to the application or to Windows itself.</span></span>

<span data-ttu-id="569cc-126">На кнопке маски группируются, чтобы определить, какие типы событий будут обрабатываться контекстом.</span><span class="sxs-lookup"><span data-stu-id="569cc-126">The button masks together determine what kinds of events will be processed by the context.</span></span>

## <a name="requirements"></a><span data-ttu-id="569cc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="569cc-127">Requirements</span></span>



| <span data-ttu-id="569cc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="569cc-128">Requirement</span></span> | <span data-ttu-id="569cc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="569cc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="569cc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="569cc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="569cc-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="569cc-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="569cc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="569cc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="569cc-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="569cc-133">None supported</span></span><br/>                                     |



 

 





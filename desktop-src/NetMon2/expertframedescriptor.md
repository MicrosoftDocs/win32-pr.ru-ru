---
description: Структура ЕКСПЕРТФРАМЕДЕСКРИПТОР содержит сведения о кадре. Когда эксперт успешно вызывает функцию Експертжетфраме, сетевой монитор передает структуру ЕКСПЕРТФРАМЕДЕСКРИПТОР обратно эксперту.
ms.assetid: 6cf99498-3cf9-46da-b6a0-3012229f6908
title: Структура ЕКСПЕРТФРАМЕДЕСКРИПТОР (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTFRAMEDESCRIPTOR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 98bafae39819b16b479df22fe6560888ef15d8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497007"
---
# <a name="expertframedescriptor-structure"></a><span data-ttu-id="d64a0-104">Структура ЕКСПЕРТФРАМЕДЕСКРИПТОР</span><span class="sxs-lookup"><span data-stu-id="d64a0-104">EXPERTFRAMEDESCRIPTOR structure</span></span>

<span data-ttu-id="d64a0-105">Структура **експертфрамедескриптор** содержит сведения о кадре.</span><span class="sxs-lookup"><span data-stu-id="d64a0-105">The **EXPERTFRAMEDESCRIPTOR** structure contains information about a frame.</span></span> <span data-ttu-id="d64a0-106">Когда эксперт успешно вызывает функцию [**експертжетфраме**](expertgetframe.md) , сетевой монитор передает структуру **експертфрамедескриптор** обратно эксперту.</span><span class="sxs-lookup"><span data-stu-id="d64a0-106">When the expert calls the [**ExpertGetFrame**](expertgetframe.md) function successfully, Network Monitor passes the **EXPERTFRAMEDESCRIPTOR** structure back to the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64a0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d64a0-107">Syntax</span></span>


```C++
typedef struct {
  DWORD                FrameNumber;
  HFRAME               hFrame;
  ULPFRAME             pFrame;
  LPRECOGNIZEDATATABLE lpRecognizeDataTable;
  LPPROPERTYTABLE      lpPropertyTable;
} EXPERTFRAMEDESCRIPTOR, *LPEXPERTFRAMEDESCRIPTOR;
```



## <a name="members"></a><span data-ttu-id="d64a0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d64a0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d64a0-109">**фраменумбер**</span><span class="sxs-lookup"><span data-stu-id="d64a0-109">**FrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d64a0-110">Номер указанного кадра.</span><span class="sxs-lookup"><span data-stu-id="d64a0-110">Number of a specified frame.</span></span>

</dd> <dt>

<span data-ttu-id="d64a0-111">**хфраме**</span><span class="sxs-lookup"><span data-stu-id="d64a0-111">**hFrame**</span></span>
</dt> <dd>

<span data-ttu-id="d64a0-112">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="d64a0-112">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d64a0-113">**пфраме**</span><span class="sxs-lookup"><span data-stu-id="d64a0-113">**pFrame**</span></span>
</dt> <dd>

<span data-ttu-id="d64a0-114">Указатель на необработанный кадр.</span><span class="sxs-lookup"><span data-stu-id="d64a0-114">Pointer to a raw frame.</span></span>

</dd> <dt>

<span data-ttu-id="d64a0-115">**лпрекогнизедататабле**</span><span class="sxs-lookup"><span data-stu-id="d64a0-115">**lpRecognizeDataTable**</span></span>
</dt> <dd>

<span data-ttu-id="d64a0-116">Таблица, указывающая, где каждый синтаксический анализатор определяет начало данных.</span><span class="sxs-lookup"><span data-stu-id="d64a0-116">Table that indicates where each parser identifies the start of the data.</span></span>

</dd> <dt>

<span data-ttu-id="d64a0-117">**лппропертитабле**</span><span class="sxs-lookup"><span data-stu-id="d64a0-117">**lpPropertyTable**</span></span>
</dt> <dd>

<span data-ttu-id="d64a0-118">Таблица свойств кадра, идентифицируемая синтаксическим анализатором.</span><span class="sxs-lookup"><span data-stu-id="d64a0-118">Table of frame properties that the parser identifies.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d64a0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d64a0-119">Remarks</span></span>

<span data-ttu-id="d64a0-120">Если эксперт задает ФЛАГи \_ присоединения \_ свойств при вызове [**експертжетфраме**](expertgetframe.md), то элемент **сзпропертитекст** в каждой структуре [**пропертинст**](propertyinst.md) имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d64a0-120">If the expert specifies FLAGS\_ATTACH\_PROPERTIES when calling [**ExpertGetFrame**](expertgetframe.md), then the **szPropertyText** member in each [**PROPERTYINST**](propertyinst.md) structure is **NULL**.</span></span>

<span data-ttu-id="d64a0-121">Если эксперт не задает ФЛАГи \_ присоединения \_ свойств при вызове функции [**експертжетфраме**](expertgetframe.md) , то элемент **лппропертитабле** имеет **значение NULL** при возврате.</span><span class="sxs-lookup"><span data-stu-id="d64a0-121">If the expert does not specify FLAGS\_ATTACH\_PROPERTIES when calling the [**ExpertGetFrame**](expertgetframe.md) function, then the **lpPropertyTable** member is **NULL** on return.</span></span>

## <a name="requirements"></a><span data-ttu-id="d64a0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d64a0-122">Requirements</span></span>



| <span data-ttu-id="d64a0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d64a0-123">Requirement</span></span> | <span data-ttu-id="d64a0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d64a0-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d64a0-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d64a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d64a0-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d64a0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d64a0-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d64a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d64a0-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d64a0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d64a0-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d64a0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d64a0-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d64a0-130"><dt>Netmon.h</dt></span></span> </dl> |



 

 





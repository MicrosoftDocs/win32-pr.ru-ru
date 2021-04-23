---
description: Содержит данные, описывающие эксперт при запуске.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Структура ЕКСПЕРТСТАРТУПИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990914"
---
# <a name="expertstartupinfo-structure"></a><span data-ttu-id="29cdf-103">Структура ЕКСПЕРТСТАРТУПИНФО</span><span class="sxs-lookup"><span data-stu-id="29cdf-103">EXPERTSTARTUPINFO structure</span></span>

<span data-ttu-id="29cdf-104">Структура **експертстартупинфо** содержит данные, описывающие эксперт при запуске.</span><span class="sxs-lookup"><span data-stu-id="29cdf-104">The **EXPERTSTARTUPINFO** structure contains data that describes an expert when it starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="29cdf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29cdf-105">Syntax</span></span>


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a><span data-ttu-id="29cdf-106">Члены</span><span class="sxs-lookup"><span data-stu-id="29cdf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="29cdf-107">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="29cdf-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-108">Флаги, описывающие эксперт.</span><span class="sxs-lookup"><span data-stu-id="29cdf-108">Flags that describe the expert.</span></span>

</dd> <dt>

<span data-ttu-id="29cdf-109">**хкаптуре**</span><span class="sxs-lookup"><span data-stu-id="29cdf-109">**hCapture**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-110">Обработчик для записи.</span><span class="sxs-lookup"><span data-stu-id="29cdf-110">Handle to a capture.</span></span>

</dd> <dt>

<span data-ttu-id="29cdf-111">**сзкаптурефиле**</span><span class="sxs-lookup"><span data-stu-id="29cdf-111">**szCaptureFile**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-112">Имя файла записи.</span><span class="sxs-lookup"><span data-stu-id="29cdf-112">Name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="29cdf-113">**двфраменумбер**</span><span class="sxs-lookup"><span data-stu-id="29cdf-113">**dwFrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-114">Номер кадра.</span><span class="sxs-lookup"><span data-stu-id="29cdf-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="29cdf-115">**хпротокол**</span><span class="sxs-lookup"><span data-stu-id="29cdf-115">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-116">Обработчик для протокола.</span><span class="sxs-lookup"><span data-stu-id="29cdf-116">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="29cdf-117">**лппропертинст**</span><span class="sxs-lookup"><span data-stu-id="29cdf-117">**lpPropertyInst**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-118">Указатель на структуру [**пропертинст**](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="29cdf-118">Pointer to a [**PROPERTYINST**](propertyinst.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="29cdf-119">**сбитфиелд**</span><span class="sxs-lookup"><span data-stu-id="29cdf-119">**sBitfield**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29cdf-120">**битнумбер**</span><span class="sxs-lookup"><span data-stu-id="29cdf-120">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-121">Используется только в том случае, если элементу **квалификатора** данных структуры [**пропертинст**](propertyinst.md) задано значение Prop \_ куал \_ flags.</span><span class="sxs-lookup"><span data-stu-id="29cdf-121">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="29cdf-122">**Системе**</span><span class="sxs-lookup"><span data-stu-id="29cdf-122">**bOn**</span></span>
</dt> <dd>

<span data-ttu-id="29cdf-123">Используется только в том случае, если элементу **квалификатора** данных структуры [**пропертинст**](propertyinst.md) задано значение Prop \_ куал \_ flags.</span><span class="sxs-lookup"><span data-stu-id="29cdf-123">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29cdf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="29cdf-124">Requirements</span></span>



| <span data-ttu-id="29cdf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="29cdf-125">Requirement</span></span> | <span data-ttu-id="29cdf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="29cdf-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29cdf-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29cdf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29cdf-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29cdf-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="29cdf-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29cdf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29cdf-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="29cdf-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="29cdf-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="29cdf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="29cdf-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="29cdf-132"><dt>Netmon.h</dt></span></span> </dl> |



 

 





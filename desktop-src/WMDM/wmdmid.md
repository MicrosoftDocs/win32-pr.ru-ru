---
title: Структура ВМДМИД
description: Структура ВМДМИД описывает серийные номера и идентификаторы групп.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Структура ВМДМИД Windows Media диспетчер устройств
- Указатель структуры ПВМДМИД Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699126"
---
# <a name="wmdmid-structure"></a><span data-ttu-id="c17f9-105">Структура ВМДМИД</span><span class="sxs-lookup"><span data-stu-id="c17f9-105">WMDMID structure</span></span>

<span data-ttu-id="c17f9-106">Структура **вмдмид** описывает серийные номера и идентификаторы групп.</span><span class="sxs-lookup"><span data-stu-id="c17f9-106">The **WMDMID** structure describes serial numbers and group IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c17f9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c17f9-107">Syntax</span></span>


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a><span data-ttu-id="c17f9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c17f9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c17f9-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="c17f9-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="c17f9-110">Размер структуры **вмдмид** в байтах.</span><span class="sxs-lookup"><span data-stu-id="c17f9-110">Size of the **WMDMID** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c17f9-111">**дввендорид**</span><span class="sxs-lookup"><span data-stu-id="c17f9-111">**dwVendorID**</span></span>
</dt> <dd>

<span data-ttu-id="c17f9-112">Значение **типа DWORD** , содержащее зарегистрированный идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="c17f9-112">**DWORD** containing the registered ID number of the vendor.</span></span> <span data-ttu-id="c17f9-113">Содержит ноль, если не используется.</span><span class="sxs-lookup"><span data-stu-id="c17f9-113">Contains zero if not in use.</span></span>

</dd> <dt>

<span data-ttu-id="c17f9-114">**\[Длина pID вмдмид \_\]**</span><span class="sxs-lookup"><span data-stu-id="c17f9-114">**pID\[WMDMID\_LENGTH\]**</span></span>
</dt> <dd>

<span data-ttu-id="c17f9-115">Указатель на массив байтов, содержащий серийный номер.</span><span class="sxs-lookup"><span data-stu-id="c17f9-115">Pointer to an array of bytes containing the serial number.</span></span> <span data-ttu-id="c17f9-116">Серийный номер — это строка байтовых значений, не имеющая стандартного формата.</span><span class="sxs-lookup"><span data-stu-id="c17f9-116">The serial number is a string of byte values that have no standard format.</span></span> <span data-ttu-id="c17f9-117">Обратите внимание, что это значение не является расширенным символом.</span><span class="sxs-lookup"><span data-stu-id="c17f9-117">Note that this is not a wide-character value.</span></span> <span data-ttu-id="c17f9-118">**Вмдмид \_ LENGTH** — это постоянное значение, определенное в мсвмдм. h.</span><span class="sxs-lookup"><span data-stu-id="c17f9-118">**WMDMID\_LENGTH** is a constant value defined in mswmdm.h.</span></span>

</dd> <dt>

<span data-ttu-id="c17f9-119">**сериалнумберленгс**</span><span class="sxs-lookup"><span data-stu-id="c17f9-119">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="c17f9-120">Фактическая длина возвращенного серийного номера в байтах.</span><span class="sxs-lookup"><span data-stu-id="c17f9-120">Actual length of the serial number returned, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c17f9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c17f9-121">Requirements</span></span>



| <span data-ttu-id="c17f9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c17f9-122">Requirement</span></span> | <span data-ttu-id="c17f9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c17f9-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c17f9-124">Header</span><span class="sxs-lookup"><span data-stu-id="c17f9-124">Header</span></span><br/> | <dl> <span data-ttu-id="c17f9-125"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c17f9-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c17f9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c17f9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c17f9-127">**Имдспдевице:: Жетсериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="c17f9-127">**IMDSPDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="c17f9-128">**Имдспсторажеглобалс:: Жетсериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="c17f9-128">**IMDSPStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="c17f9-129">**Ивмдмдевице:: Жетсериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="c17f9-129">**IWMDMDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="c17f9-130">**Ивмдмсторажеглобалс:: Жетсериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="c17f9-130">**IWMDMStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="c17f9-131">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="c17f9-131">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 






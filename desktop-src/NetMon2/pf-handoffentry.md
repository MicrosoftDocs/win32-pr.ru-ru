---
description: Структура PF \_ хандоффентри определяет протокол, который сетевой монитор добавляет к переданному набору средства синтаксического анализа.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Структура PF_HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674038"
---
# <a name="pf_handoffentry-structure"></a><span data-ttu-id="b0aea-103">\_Структура PF хандоффентри</span><span class="sxs-lookup"><span data-stu-id="b0aea-103">PF\_HANDOFFENTRY structure</span></span>

<span data-ttu-id="b0aea-104">Структура **PF \_ хандоффентри** определяет протокол, который сетевой монитор добавляет к переданному набору средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="b0aea-104">The **PF\_HANDOFFENTRY** structure defines a protocol that Network Monitor adds to the handoff set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0aea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0aea-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="b0aea-106">Члены</span><span class="sxs-lookup"><span data-stu-id="b0aea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0aea-107">**сзинифиле**</span><span class="sxs-lookup"><span data-stu-id="b0aea-107">**szIniFile**</span></span>
</dt> <dd>

<span data-ttu-id="b0aea-108">Имя INI-файла, связанного с протоколом.</span><span class="sxs-lookup"><span data-stu-id="b0aea-108">Name of the INI file associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0aea-109">**сзинисектион**</span><span class="sxs-lookup"><span data-stu-id="b0aea-109">**szIniSection**</span></span>
</dt> <dd>

<span data-ttu-id="b0aea-110">Метка раздела в INI-файле.</span><span class="sxs-lookup"><span data-stu-id="b0aea-110">Section label within the INI file.</span></span>

</dd> <dt>

<span data-ttu-id="b0aea-111">**сзпротокол**</span><span class="sxs-lookup"><span data-stu-id="b0aea-111">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="b0aea-112">Имя протокола.</span><span class="sxs-lookup"><span data-stu-id="b0aea-112">Name of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0aea-113">**двхандоффвалуе**</span><span class="sxs-lookup"><span data-stu-id="b0aea-113">**dwHandOffValue**</span></span>
</dt> <dd>

<span data-ttu-id="b0aea-114">Значение, связанное с протоколом.</span><span class="sxs-lookup"><span data-stu-id="b0aea-114">Value associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0aea-115">**валуеформатбасе**</span><span class="sxs-lookup"><span data-stu-id="b0aea-115">**ValueFormatBase**</span></span>
</dt> <dd>

<span data-ttu-id="b0aea-116">Основание числового значения протокола, указанного в **двхандоффвалуе**.</span><span class="sxs-lookup"><span data-stu-id="b0aea-116">Numeric base of the protocol value that is specified in **dwHandOffValue**.</span></span> <span data-ttu-id="b0aea-117">Для функции **валуеформатбасе** необходимо задать один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="b0aea-117">The **ValueFormatBase** function must be set to one of the following:</span></span>



| <span data-ttu-id="b0aea-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b0aea-118">Value</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="b0aea-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b0aea-119">Meaning</span></span>                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <span data-ttu-id="b0aea-120"><dt>**формат переданного \_ значения является \_ \_ \_ неизвестным**</dt></span><span class="sxs-lookup"><span data-stu-id="b0aea-120"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="b0aea-121">Неизвестный базовый</span><span class="sxs-lookup"><span data-stu-id="b0aea-121">Unknown base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <span data-ttu-id="b0aea-122"><dt>**формат переданного \_ значения — \_ \_ базовое \_ десятичное**</dt></span><span class="sxs-lookup"><span data-stu-id="b0aea-122"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_DECIMAL**</dt></span></span> </dl> | <span data-ttu-id="b0aea-123">Основание десятичного разделителя</span><span class="sxs-lookup"><span data-stu-id="b0aea-123">Decimal base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <span data-ttu-id="b0aea-124"><dt>**формат переданного \_ значения, \_ \_ Базовый \_ Шестнадцатеричный**</dt></span><span class="sxs-lookup"><span data-stu-id="b0aea-124"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_HEX**</dt></span></span> </dl>             | <span data-ttu-id="b0aea-125">Основание шестнадцатеричного</span><span class="sxs-lookup"><span data-stu-id="b0aea-125">Hexadecimal base</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0aea-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0aea-126">Remarks</span></span>

<span data-ttu-id="b0aea-127">Массив структур **PF \_ хандоффентри** используется в структуре [PF \_ хандоффсет](pf-handoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="b0aea-127">An array of the **PF\_HANDOFFENTRY** structures is used in the [PF\_HANDOFFSET](pf-handoffset.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0aea-128">Требования</span><span class="sxs-lookup"><span data-stu-id="b0aea-128">Requirements</span></span>



| <span data-ttu-id="b0aea-129">Требование</span><span class="sxs-lookup"><span data-stu-id="b0aea-129">Requirement</span></span> | <span data-ttu-id="b0aea-130">Значение</span><span class="sxs-lookup"><span data-stu-id="b0aea-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0aea-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0aea-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b0aea-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0aea-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b0aea-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0aea-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b0aea-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0aea-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b0aea-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b0aea-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0aea-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0aea-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0aea-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0aea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0aea-138">PF \_ хандоффсет</span><span class="sxs-lookup"><span data-stu-id="b0aea-138">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> </dl>

 

 





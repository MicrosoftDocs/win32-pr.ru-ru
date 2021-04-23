---
description: Указывает тип шины ввода-вывода, используемой графическим адаптером.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Перечисление D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710827"
---
# <a name="d3dbustype-enumeration"></a><span data-ttu-id="af6ba-103">Перечисление D3DBUSTYPE</span><span class="sxs-lookup"><span data-stu-id="af6ba-103">D3DBUSTYPE enumeration</span></span>

<span data-ttu-id="af6ba-104">Указывает тип шины ввода-вывода, используемой графическим адаптером.</span><span class="sxs-lookup"><span data-stu-id="af6ba-104">Specifies the type of I/O bus used by the graphics adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af6ba-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a><span data-ttu-id="af6ba-106">Константы</span><span class="sxs-lookup"><span data-stu-id="af6ba-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="af6ba-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="af6ba-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE\_OTHER**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-108">Указывает тип шины, отличный от перечисленных здесь типов.</span><span class="sxs-lookup"><span data-stu-id="af6ba-108">Indicates a type of bus other than the types listed here.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="af6ba-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE\_PCI**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-110">Шина PCI.</span><span class="sxs-lookup"><span data-stu-id="af6ba-110">PCI bus.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ пЦикс**</span><span class="sxs-lookup"><span data-stu-id="af6ba-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE\_PCIX**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-112">Шина PCI-X.</span><span class="sxs-lookup"><span data-stu-id="af6ba-112">PCI-X bus.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ пЦиекспресс**</span><span class="sxs-lookup"><span data-stu-id="af6ba-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE\_PCIEXPRESS**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-114">Шина PCI Express.</span><span class="sxs-lookup"><span data-stu-id="af6ba-114">PCI Express bus.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**</span><span class="sxs-lookup"><span data-stu-id="af6ba-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE\_AGP**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-116">Шина ускорения графического порта (AGP).</span><span class="sxs-lookup"><span data-stu-id="af6ba-116">Accelerated Graphics Port (AGP) bus.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Модификатор D3DBUSIMPL \_ в \_ \_ наборе микросхем**</span><span class="sxs-lookup"><span data-stu-id="af6ba-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL\_MODIFIER\_INSIDE\_OF\_CHIPSET**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-118">Реализация графического адаптера входит в Северный мост набора микросхем материнской платы.</span><span class="sxs-lookup"><span data-stu-id="af6ba-118">The implementation for the graphics adapter is in a motherboard chipset's north bridge.</span></span> <span data-ttu-id="af6ba-119">Этот флаг подразумевает, что данные никогда не передаются через шину расширения (например, PCI или AGP) при передаче из основной памяти в графический адаптер.</span><span class="sxs-lookup"><span data-stu-id="af6ba-119">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**\_Модификатор D3DBUSIMPL \_ отслеживает \_ на \_ \_ плате \_ \_ микросхемы**</span><span class="sxs-lookup"><span data-stu-id="af6ba-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_CHIP**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-121">Указывает, что графический адаптер подключен к северному мосту набора микросхем материнской платы с помощью дорожек на материнской плате, и все микросхемы графического адаптера помещаются на материнскую плату.</span><span class="sxs-lookup"><span data-stu-id="af6ba-121">Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard.</span></span> <span data-ttu-id="af6ba-122">Этот флаг подразумевает, что данные никогда не передаются через шину расширения (например, PCI или AGP) при передаче из основной памяти в графический адаптер.</span><span class="sxs-lookup"><span data-stu-id="af6ba-122">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**\_Модификатор D3DBUSIMPL \_ отслеживает \_ на \_ \_ плате 8 \_ на \_ сокете**</span><span class="sxs-lookup"><span data-stu-id="af6ba-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_SOCKET**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-124">Графический адаптер подключен к северному мосту набора микросхем материнской платы с помощью дорожек на материнской плате, и все микросхемы графического адаптера подключены к материнской плате через сокеты.</span><span class="sxs-lookup"><span data-stu-id="af6ba-124">The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_ \_ Соединитель дочерней \_ платы модификатора D3DBUSIMPL \_**</span><span class="sxs-lookup"><span data-stu-id="af6ba-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-126">Графический адаптер подключен к материнской плате через соединитель даугхтербоард.</span><span class="sxs-lookup"><span data-stu-id="af6ba-126">The graphics adapter is connected to the motherboard through a daughterboard connector.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ Соединитель дочерней платы модификатора D3DBUSIMPL \_ \_ \_ внутри \_ \_ Нуае**</span><span class="sxs-lookup"><span data-stu-id="af6ba-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR\_INSIDE\_OF\_NUAE**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-128">Графический адаптер подключен к материнской плате через соединитель даугхтербоард, и графический адаптер находится внутри корпуса, который не доступен пользователю.</span><span class="sxs-lookup"><span data-stu-id="af6ba-128">The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.</span></span>

</dd> <dt>

<span data-ttu-id="af6ba-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Модификатор D3DBUSIMPL \_ не является \_ стандартным**</span><span class="sxs-lookup"><span data-stu-id="af6ba-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL\_MODIFIER\_NON\_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="af6ba-130">Задан один из флагов модификатора D3DBUSIMPL \_ \_ \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="af6ba-130">One of the D3DBUSIMPL\_MODIFIER\_MODIFIER\_Xxx flags is set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af6ba-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af6ba-131">Remarks</span></span>

<span data-ttu-id="af6ba-132">Можно задать до трех флагов.</span><span class="sxs-lookup"><span data-stu-id="af6ba-132">As many as three flags can be set.</span></span> <span data-ttu-id="af6ba-133">Флаги в диапазоне от 0x00 до 0x04 (**D3DBUSTYPE \_ xxx**) предоставляют базовый тип шины.</span><span class="sxs-lookup"><span data-stu-id="af6ba-133">Flags in the range 0x00 through 0x04 (**D3DBUSTYPE\_Xxx**) provide the basic bus type.</span></span> <span data-ttu-id="af6ba-134">Флаги в диапазоне от 0x10000 до 0x50000 **( \_ Модификатор D3DBUSIMPL \_ xxx**) изменяют базовое описание.</span><span class="sxs-lookup"><span data-stu-id="af6ba-134">Flags in the range 0x10000 through 0x50000 (**D3DBUSIMPL\_MODIFIER\_Xxx**) modify the basic description.</span></span> <span data-ttu-id="af6ba-135">Драйвер устанавливает один флаг типа Bus и может устанавливать ноль или один флаг модификатора.</span><span class="sxs-lookup"><span data-stu-id="af6ba-135">The driver sets one bus-type flag, and can set zero or one modifier flag.</span></span> <span data-ttu-id="af6ba-136">Если драйвер задает флаг модификатора, он также задает **\_ \_ \_ нестандартный флаг модификатора D3DBUSIMPL** .</span><span class="sxs-lookup"><span data-stu-id="af6ba-136">If the driver sets a modifier flag, it also sets the **D3DBUSIMPL\_MODIFIER\_NON\_STANDARD** flag.</span></span> <span data-ttu-id="af6ba-137">Флаги объединяются с побитовой **или**.</span><span class="sxs-lookup"><span data-stu-id="af6ba-137">Flags are combined with a bitwise **OR**.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6ba-138">Требования</span><span class="sxs-lookup"><span data-stu-id="af6ba-138">Requirements</span></span>



| <span data-ttu-id="af6ba-139">Требование</span><span class="sxs-lookup"><span data-stu-id="af6ba-139">Requirement</span></span> | <span data-ttu-id="af6ba-140">Значение</span><span class="sxs-lookup"><span data-stu-id="af6ba-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af6ba-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af6ba-141">Minimum supported client</span></span><br/> | <span data-ttu-id="af6ba-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="af6ba-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="af6ba-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af6ba-143">Minimum supported server</span></span><br/> | <span data-ttu-id="af6ba-144">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="af6ba-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="af6ba-145">Header</span><span class="sxs-lookup"><span data-stu-id="af6ba-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="af6ba-146"><dt>D3d9types. h (включение D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af6ba-146"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af6ba-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af6ba-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6ba-148">Перечисления видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="af6ba-148">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 





---
title: Перечисление Вмсериалпорттипе (Впккоминтерфацес. h)
description: Указывает тип последовательного порта.
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- Перечисление Вмсериалпорттипе Virtual PC
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534757"
---
# <a name="vmserialporttype-enumeration"></a><span data-ttu-id="ffb42-104">Перечисление Вмсериалпорттипе</span><span class="sxs-lookup"><span data-stu-id="ffb42-104">VMSerialPortType enumeration</span></span>

<span data-ttu-id="ffb42-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ffb42-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ffb42-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ffb42-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ffb42-107">Указывает тип последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="ffb42-107">Specifies the type of serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb42-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffb42-108">Syntax</span></span>


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a><span data-ttu-id="ffb42-109">Константы</span><span class="sxs-lookup"><span data-stu-id="ffb42-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ffb42-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**Вмсериалпорт \_ хостпорт**</span><span class="sxs-lookup"><span data-stu-id="ffb42-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort\_HostPort**</span></span>
</dt> <dd>

<span data-ttu-id="ffb42-111">Последовательный порт узла.</span><span class="sxs-lookup"><span data-stu-id="ffb42-111">A host serial port.</span></span>

</dd> <dt>

<span data-ttu-id="ffb42-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**Вмсериалпорт \_ TextFile**</span><span class="sxs-lookup"><span data-stu-id="ffb42-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort\_TextFile**</span></span>
</dt> <dd>

<span data-ttu-id="ffb42-113">Текстовый файл узла.</span><span class="sxs-lookup"><span data-stu-id="ffb42-113">A host text file.</span></span>

</dd> <dt>

<span data-ttu-id="ffb42-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**Вмсериалпорт \_ помощью канала NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="ffb42-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="ffb42-115">Именованный канал.</span><span class="sxs-lookup"><span data-stu-id="ffb42-115">A named pipe.</span></span>

</dd> <dt>

<span data-ttu-id="ffb42-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**Вмсериалпорт \_ null**</span><span class="sxs-lookup"><span data-stu-id="ffb42-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="ffb42-117">Последовательный порт, **равный null** (отклоняет все отправленные на него биты).</span><span class="sxs-lookup"><span data-stu-id="ffb42-117">A **NULL** serial port (discards all bits sent to it).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffb42-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ffb42-118">Requirements</span></span>



| <span data-ttu-id="ffb42-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ffb42-119">Requirement</span></span> | <span data-ttu-id="ffb42-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb42-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb42-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffb42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb42-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ffb42-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffb42-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffb42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb42-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ffb42-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ffb42-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ffb42-125">End of client support</span></span><br/>    | <span data-ttu-id="ffb42-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ffb42-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ffb42-127">Продукт</span><span class="sxs-lookup"><span data-stu-id="ffb42-127">Product</span></span><br/>                  | <span data-ttu-id="ffb42-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ffb42-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ffb42-129">Header</span><span class="sxs-lookup"><span data-stu-id="ffb42-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffb42-130"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb42-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffb42-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffb42-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb42-132">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="ffb42-132">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 


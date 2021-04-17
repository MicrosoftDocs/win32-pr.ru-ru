---
description: Структура СТАТИОНКУЕРИ предоставляет сведения о конкретном компьютере, использующем сетевой монитор.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Структура СТАТИОНКУЕРИ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673539"
---
# <a name="stationquery-structure"></a><span data-ttu-id="5ed53-103">Структура СТАТИОНКУЕРИ</span><span class="sxs-lookup"><span data-stu-id="5ed53-103">STATIONQUERY structure</span></span>

<span data-ttu-id="5ed53-104">Структура **статионкуери** предоставляет сведения о конкретном компьютере, использующем сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5ed53-104">The **STATIONQUERY** structure provides information about a specific computer using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ed53-105">Syntax</span></span>


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a><span data-ttu-id="5ed53-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5ed53-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ed53-107">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="5ed53-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-108">Флаги, которые указывают текущее состояние сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="5ed53-108">Flags that Identify the current state of Network Monitor.</span></span>



| <span data-ttu-id="5ed53-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5ed53-109">Value</span></span>                                                                                                                                                                                                                | <span data-ttu-id="5ed53-110">Значение</span><span class="sxs-lookup"><span data-stu-id="5ed53-110">Meaning</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <span data-ttu-id="5ed53-111"><dt>**\_Флаги статионкуери \_ загружены**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed53-111"><dt>**STATIONQUERY\_FLAGS\_LOADED**</dt></span></span> </dl>                   | <span data-ttu-id="5ed53-112">Драйвер загружен, но не является ядром.</span><span class="sxs-lookup"><span data-stu-id="5ed53-112">The driver is loaded, but the kernel is not.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <span data-ttu-id="5ed53-113"><dt>**СТАТИОНКУЕРИные \_ Флаги \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed53-113"><dt>**STATIONQUERY\_FLAGS\_RUNNING**</dt></span></span> </dl>                | <span data-ttu-id="5ed53-114">Драйвер загружен, но не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="5ed53-114">The driver is loaded but not capturing data.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <span data-ttu-id="5ed53-115"><dt>**\_захват флагов статионкуери \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed53-115"><dt>**STATIONQUERY\_FLAGS\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="5ed53-116">Драйвер активно вовлечен в захват.</span><span class="sxs-lookup"><span data-stu-id="5ed53-116">The driver is actively engaged in a capture.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <span data-ttu-id="5ed53-117"><dt>**\_Передача флагов статионкуери \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed53-117"><dt>**STATIONQUERY\_FLAGS\_TRANSMITTING**</dt></span></span> </dl> | <span data-ttu-id="5ed53-118">Этот флаг устарел.</span><span class="sxs-lookup"><span data-stu-id="5ed53-118">This flag is obsolete.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="5ed53-119">**бкдверминор**</span><span class="sxs-lookup"><span data-stu-id="5ed53-119">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-120">Дополнительный номер версии сетевой монитор, установленного на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ed53-120">Minor version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-121">**бкдвермажор**</span><span class="sxs-lookup"><span data-stu-id="5ed53-121">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-122">Основной номер версии сетевой монитор, установленной на компьютере.</span><span class="sxs-lookup"><span data-stu-id="5ed53-122">Major version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-123">**лиценсенумбер**</span><span class="sxs-lookup"><span data-stu-id="5ed53-123">**LicenseNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-124">Номер лицензии на программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="5ed53-124">Software license number.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-125">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="5ed53-125">**MachineName**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-126">Имя изготовителя компьютера (при наличии).</span><span class="sxs-lookup"><span data-stu-id="5ed53-126">Computer manufacturer name, if any.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-127">**UserName**</span><span class="sxs-lookup"><span data-stu-id="5ed53-127">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-128">Имя пользователя или идентификатор системы.</span><span class="sxs-lookup"><span data-stu-id="5ed53-128">User name or system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-129">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="5ed53-129">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-130">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="5ed53-130">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-131">**адаптераддресс**</span><span class="sxs-lookup"><span data-stu-id="5ed53-131">**AdapterAddress**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-132">Адрес сетевой карты.</span><span class="sxs-lookup"><span data-stu-id="5ed53-132">NIC address.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-133">**вмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="5ed53-133">**WMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-134">Имя компьютера в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="5ed53-134">Unicode computer name.</span></span> <span data-ttu-id="5ed53-135">Этот элемент применяется к сетевой монитор 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5ed53-135">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="5ed53-136">**вусернаме**</span><span class="sxs-lookup"><span data-stu-id="5ed53-136">**WUserName**</span></span>
</dt> <dd>

<span data-ttu-id="5ed53-137">Имя пользователя в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="5ed53-137">Unicode user name.</span></span> <span data-ttu-id="5ed53-138">Этот элемент применяется к сетевой монитор 2,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5ed53-138">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ed53-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ed53-139">Remarks</span></span>

<span data-ttu-id="5ed53-140">Массив этих структур используется структурой [куеритабле](querytable.md) для предоставления списка компьютеров, которые в настоящее время используют сетевой монитор для сбора данных.</span><span class="sxs-lookup"><span data-stu-id="5ed53-140">An array of these structures is used by the [QUERYTABLE](querytable.md) structure to provide a list of the computers that are currently using Network Monitor to capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed53-141">Требования</span><span class="sxs-lookup"><span data-stu-id="5ed53-141">Requirements</span></span>



| <span data-ttu-id="5ed53-142">Требование</span><span class="sxs-lookup"><span data-stu-id="5ed53-142">Requirement</span></span> | <span data-ttu-id="5ed53-143">Значение</span><span class="sxs-lookup"><span data-stu-id="5ed53-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed53-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ed53-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed53-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ed53-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5ed53-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ed53-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed53-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5ed53-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5ed53-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5ed53-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed53-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ed53-149"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed53-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ed53-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed53-151">куеритабле</span><span class="sxs-lookup"><span data-stu-id="5ed53-151">QUERYTABLE</span></span>](querytable.md)
</dt> </dl>

 

 





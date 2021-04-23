---
description: Структура НЕТВОРКИНФО описывает сетевую карту.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Структура НЕТВОРКИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818529"
---
# <a name="networkinfo-structure"></a><span data-ttu-id="3cb8e-103">Структура НЕТВОРКИНФО</span><span class="sxs-lookup"><span data-stu-id="3cb8e-103">NETWORKINFO structure</span></span>

<span data-ttu-id="3cb8e-104">Структура НЕТВОРКИНФО описывает сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-104">The NETWORKINFO structure describes a NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb8e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cb8e-105">Syntax</span></span>


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a><span data-ttu-id="3cb8e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3cb8e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3cb8e-107">**перманентаддр**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-107">**PermanentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-108">Постоянный MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-108">Permanent MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-109">**куррентаддр**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-109">**CurrentAddr**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-110">Текущий MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-110">Current MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-111">**OtherAddress**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-111">**OtherAddress**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-112">Другой адрес, поддерживающий эту возможность (например, IP, IPX).</span><span class="sxs-lookup"><span data-stu-id="3cb8e-112">Other address that support this (for example IP, IPX).</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-113">**LinkSpeed**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-113">**LinkSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-114">Скорость связи в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-114">Link speed, in Mbps.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-116">Тип носителя.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-116">Media type.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-117">**MaxFrameSize**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-117">**MaxFrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-118">Максимально допустимый размер кадра.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-118">Maximum frame size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-119">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-120">Этот параметр может иметь один из следующих информационных флагов:</span><span class="sxs-lookup"><span data-stu-id="3cb8e-120">This parameter can be one of the following informational flags:</span></span>



| <span data-ttu-id="3cb8e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb8e-121">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="3cb8e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb8e-122">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <span data-ttu-id="3cb8e-123"><dt>**\_Флаги нетворкинфо \_ пмоде \_ не \_ поддерживаются**</dt></span><span class="sxs-lookup"><span data-stu-id="3cb8e-123"><dt>**NETWORKINFO\_FLAGS\_PMODE\_NOT\_SUPPORTED**</dt></span></span> </dl>    | <span data-ttu-id="3cb8e-124">Сетевой адаптер не поддерживает неизбирательный режим, то есть он будет записывать только трафик, который является широковещательным или включает только локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-124">The network card does not support promiscuous mode, meaning that it will only capture traffic which is broadcast in nature or only involves the local machine.</span></span><br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <span data-ttu-id="3cb8e-125"><dt>**НЕТВОРКИНФО \_ Флаги \_ RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="3cb8e-125"><dt>**NETWORKINFO\_FLAGS\_RAS**</dt></span></span> </dl>                                                      | <span data-ttu-id="3cb8e-126">Это виртуальная сетевая карта, которая является подключением к серверу удаленного доступа (RAS) через модем или другую сетевую карту.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-126">This is a virtual network card that is a RAS (Remote Access Server) connection through a modem or another network card.</span></span><br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <span data-ttu-id="3cb8e-127"><dt>**\_ \_ удаленная карта ФЛАГов нетворкинфо \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3cb8e-127"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_CARD**</dt></span></span> </dl>                             | <span data-ttu-id="3cb8e-128">Сетевая карта не находится на локальном компьютере, но записывается на удаленном компьютере в соответствии с заданной учетной записью на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-128">The network card is not on the local computer, but is capturing on a remote machine at the bequest of the local computer.</span></span><br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <span data-ttu-id="3cb8e-129"><dt>**НЕТВОРКИНФО \_ Флаги \_ удаленного \_ NAL**</dt></span><span class="sxs-lookup"><span data-stu-id="3cb8e-129"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL**</dt></span></span> </dl>                                | <span data-ttu-id="3cb8e-130">Устаревшие не используйте.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-130">Obsolete; do not use.</span></span><br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <span data-ttu-id="3cb8e-131"><dt>**НЕТВОРКИНФО \_ помечает \_ Удаленный \_ NAL \_ Connected**</dt></span><span class="sxs-lookup"><span data-stu-id="3cb8e-131"><dt>**NETWORKINFO\_FLAGS\_REMOTE\_NAL\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3cb8e-132">Устаревшие не используйте.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-132">Obsolete; do not use.</span></span><br/>                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="3cb8e-133">**тиместампскалефактор**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-133">**TimestampScaleFactor**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-134">Например, значение 1 указывает на 1/1 мс, 10 — на 1/10 мс, 100 — на 1/100 мс и т. д.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-134">For example, a value of 1 indicates 1/1 ms, 10 indicates 1/10 ms, 100 indicates 1/100 ms, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-135">**NodeName**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-135">**NodeName**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-136">Имя удаленной рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-136">Name of remote workstation.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-137">**пмодесуппортед**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-137">**PModeSupported**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-138">Индикатор поддержки сетевого интерфейса P-Mode.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-138">NIC P-mode support indicator.</span></span>

</dd> <dt>

<span data-ttu-id="3cb8e-139">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="3cb8e-139">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="3cb8e-140">Поле комментария адаптера.</span><span class="sxs-lookup"><span data-stu-id="3cb8e-140">Adapter comment field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cb8e-141">Требования</span><span class="sxs-lookup"><span data-stu-id="3cb8e-141">Requirements</span></span>



| <span data-ttu-id="3cb8e-142">Требование</span><span class="sxs-lookup"><span data-stu-id="3cb8e-142">Requirement</span></span> | <span data-ttu-id="3cb8e-143">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb8e-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb8e-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cb8e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb8e-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3cb8e-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3cb8e-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cb8e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb8e-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3cb8e-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3cb8e-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3cb8e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb8e-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb8e-149"><dt>Netmon.h</dt></span></span> </dl> |



 

 





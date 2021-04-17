---
title: Структура ВМДМРИГХТС
description: Структура ВМДМРИГХТС описывает права на использование содержимого.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Структура ВМДМРИГХТС Windows Media диспетчер устройств
- Указатель структуры ПВМДМРИГХТС Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694595"
---
# <a name="wmdmrights-structure"></a><span data-ttu-id="e38fd-105">Структура ВМДМРИГХТС</span><span class="sxs-lookup"><span data-stu-id="e38fd-105">WMDMRIGHTS structure</span></span>

<span data-ttu-id="e38fd-106">Структура **вмдмригхтс** описывает права на использование содержимого.</span><span class="sxs-lookup"><span data-stu-id="e38fd-106">The **WMDMRIGHTS** structure describes content-use rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="e38fd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e38fd-107">Syntax</span></span>


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a><span data-ttu-id="e38fd-108">Члены</span><span class="sxs-lookup"><span data-stu-id="e38fd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e38fd-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="e38fd-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="e38fd-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="e38fd-110">Size of the structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e38fd-111">**двконтенттипе**</span><span class="sxs-lookup"><span data-stu-id="e38fd-111">**dwContentType**</span></span>
</dt> <dd>

<span data-ttu-id="e38fd-112">**DWORD** , содержащий тип содержимого.</span><span class="sxs-lookup"><span data-stu-id="e38fd-112">**DWORD** containing the type of content.</span></span>

</dd> <dt>

<span data-ttu-id="e38fd-113">**фуфлагс**</span><span class="sxs-lookup"><span data-stu-id="e38fd-113">**fuFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e38fd-114">Битовое поле, указывающее параметры прав, используемые для содержимого.</span><span class="sxs-lookup"><span data-stu-id="e38fd-114">Bit field specifying the rights options in use for the content.</span></span>



| <span data-ttu-id="e38fd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e38fd-115">Value</span></span>                        | <span data-ttu-id="e38fd-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e38fd-116">Description</span></span>                                  |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="e38fd-117">ВМДМ \_ Rights \_ плайбакккаунт</span><span class="sxs-lookup"><span data-stu-id="e38fd-117">WMDM\_RIGHTS\_PLAYBACKCOUNT</span></span>  | <span data-ttu-id="e38fd-118">Количество раз, когда файл можно воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="e38fd-118">Number of times that the file can be played.</span></span> |
| <span data-ttu-id="e38fd-119">ВМДМ \_ Rights \_ EXPIRATIONDATE</span><span class="sxs-lookup"><span data-stu-id="e38fd-119">WMDM\_RIGHTS\_EXPIRATIONDATE</span></span> | <span data-ttu-id="e38fd-120">Дата окончания срока действия файла.</span><span class="sxs-lookup"><span data-stu-id="e38fd-120">Expiration date of the file.</span></span>                 |
| <span data-ttu-id="e38fd-121">ВМДМ \_ Rights \_ фрисериалидс</span><span class="sxs-lookup"><span data-stu-id="e38fd-121">WMDM\_RIGHTS\_FREESERIALIDS</span></span>  | <span data-ttu-id="e38fd-122">Бесплатный серийный идентификатор файла.</span><span class="sxs-lookup"><span data-stu-id="e38fd-122">Free serial identifier of the file.</span></span>          |
| <span data-ttu-id="e38fd-123">\_ \_ Группа GROUPID Rights вмдм</span><span class="sxs-lookup"><span data-stu-id="e38fd-123">WMDM\_RIGHTS\_GROUPID Group</span></span>  | <span data-ttu-id="e38fd-124">Идентификатор файла.</span><span class="sxs-lookup"><span data-stu-id="e38fd-124">Identifier of the file.</span></span>                      |
| <span data-ttu-id="e38fd-125">ВМДМ \_ Rights \_ намедсериалидс</span><span class="sxs-lookup"><span data-stu-id="e38fd-125">WMDM\_RIGHTS\_NAMEDSERIALIDS</span></span> | <span data-ttu-id="e38fd-126">Именованный последовательный идентификатор файла.</span><span class="sxs-lookup"><span data-stu-id="e38fd-126">Named serial identifier of the file.</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e38fd-127">**фуригхтс**</span><span class="sxs-lookup"><span data-stu-id="e38fd-127">**fuRights**</span></span>
</dt> <dd>

<span data-ttu-id="e38fd-128">Битовое поле, содержащее биты прав для содержимого.</span><span class="sxs-lookup"><span data-stu-id="e38fd-128">Bit field containing the rights bits for the content.</span></span>



| <span data-ttu-id="e38fd-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e38fd-129">Value</span></span>                                     | <span data-ttu-id="e38fd-130">Описание</span><span class="sxs-lookup"><span data-stu-id="e38fd-130">Description</span></span>                                   |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="e38fd-131">ВМДМ \_ прав \_ \_ на \_ ПК</span><span class="sxs-lookup"><span data-stu-id="e38fd-131">WMDM\_RIGHTS\_PLAY\_ON\_PC</span></span>                | <span data-ttu-id="e38fd-132">Содержимое может воспроизводиться на личном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e38fd-132">Content can be played on a personal computer.</span></span> |
| <span data-ttu-id="e38fd-133">\_Копирование прав \_ вмдм \_ на \_ устройство, не защищенное от \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="e38fd-133">WMDM\_RIGHTS\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="e38fd-134">Содержимое может быть скопировано на устройство, не поддерживающее SDMI.</span><span class="sxs-lookup"><span data-stu-id="e38fd-134">Content can be copied to a non-SDMI device.</span></span>   |
| <span data-ttu-id="e38fd-135">ВМДМ \_ прав \_ копирования \_ на \_ компакт-диск</span><span class="sxs-lookup"><span data-stu-id="e38fd-135">WMDM\_RIGHTS\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="e38fd-136">Содержимое может быть скопировано на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="e38fd-136">Content can be copied to a CD.</span></span>                |
| <span data-ttu-id="e38fd-137">\_Копирование прав \_ вмдм \_ на \_ \_ устройство SDMI</span><span class="sxs-lookup"><span data-stu-id="e38fd-137">WMDM\_RIGHTS\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="e38fd-138">Содержимое может быть скопировано на устройство SDMI.</span><span class="sxs-lookup"><span data-stu-id="e38fd-138">Content can be copied to an SDMI device.</span></span>      |



 

</dd> <dt>

<span data-ttu-id="e38fd-139">**дваппсек**</span><span class="sxs-lookup"><span data-stu-id="e38fd-139">**dwAppSec**</span></span>
</dt> <dd>

<span data-ttu-id="e38fd-140">Массив байтов, указывающий минимальный уровень безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="e38fd-140">Byte array that specifies the minimum level of application security.</span></span>

</dd> <dt>

<span data-ttu-id="e38fd-141">**двплайбакккаунт**</span><span class="sxs-lookup"><span data-stu-id="e38fd-141">**dwPlaybackCount**</span></span>
</dt> <dd>

<span data-ttu-id="e38fd-142">Значение **типа DWORD** , содержащее количество оставшихся раз, когда может быть визуализировано содержимое.</span><span class="sxs-lookup"><span data-stu-id="e38fd-142">**DWORD** containing the number of remaining times that the content can be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="e38fd-143">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="e38fd-143">**ExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="e38fd-144">Структура [**вмдмдатетиме**](wmdmdatetime.md) , содержащая дату и время окончания срока действия для содержимого.</span><span class="sxs-lookup"><span data-stu-id="e38fd-144">[**WMDMDATETIME**](wmdmdatetime.md) structure containing the expiration date and time for the content.</span></span> <span data-ttu-id="e38fd-145">Если срок действия лицензии не истек, то элементу **ВЕАР** присваивается значение 0xFFFF, а все остальные члены **вмдмдатетиме** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="e38fd-145">If the license has no expiration date, the **wYear** member is set to 0xFFFF, and all other members of **WMDMDATETIME** are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e38fd-146">Требования</span><span class="sxs-lookup"><span data-stu-id="e38fd-146">Requirements</span></span>



| <span data-ttu-id="e38fd-147">Требование</span><span class="sxs-lookup"><span data-stu-id="e38fd-147">Requirement</span></span> | <span data-ttu-id="e38fd-148">Значение</span><span class="sxs-lookup"><span data-stu-id="e38fd-148">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e38fd-149">Header</span><span class="sxs-lookup"><span data-stu-id="e38fd-149">Header</span></span><br/> | <dl> <span data-ttu-id="e38fd-150"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e38fd-150"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e38fd-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e38fd-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e38fd-152">**Имдспстораже:: направо**</span><span class="sxs-lookup"><span data-stu-id="e38fd-152">**IMDSPStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[<span data-ttu-id="e38fd-153">**Ивмдмстораже:: направо**</span><span class="sxs-lookup"><span data-stu-id="e38fd-153">**IWMDMStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[<span data-ttu-id="e38fd-154">**вмдмдатетиме**</span><span class="sxs-lookup"><span data-stu-id="e38fd-154">**WMDMDATETIME**</span></span>](wmdmdatetime.md)
</dt> <dt>

[<span data-ttu-id="e38fd-155">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="e38fd-155">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 






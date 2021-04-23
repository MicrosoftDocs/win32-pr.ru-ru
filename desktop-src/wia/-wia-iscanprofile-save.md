---
description: Сохраняет изменения профиля на диск.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'Метод Исканпрофиле:: Save (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542807"
---
# <a name="iscanprofilesave-method"></a><span data-ttu-id="7dc38-103">Метод Исканпрофиле:: Save</span><span class="sxs-lookup"><span data-stu-id="7dc38-103">IScanProfile::Save method</span></span>

<span data-ttu-id="7dc38-104">Сохраняет изменения профиля на диск.</span><span class="sxs-lookup"><span data-stu-id="7dc38-104">Saves changes to a profile to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc38-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dc38-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="7dc38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dc38-106">Parameters</span></span>

<span data-ttu-id="7dc38-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7dc38-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7dc38-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7dc38-108">Return value</span></span>

<span data-ttu-id="7dc38-109">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7dc38-109">Type: **HRESULT**</span></span>

<span data-ttu-id="7dc38-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7dc38-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7dc38-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7dc38-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc38-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7dc38-112">Remarks</span></span>

<span data-ttu-id="7dc38-113">Сохраненный профиль сканирования — это XML-файл, хранящийся в% USERPROFILE% \\ Application Data \\ \\ Center \\ усерсканпрофилес.</span><span class="sxs-lookup"><span data-stu-id="7dc38-113">A saved scan profile is an XML file stored at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="7dc38-114">Если в объект [**исканпрофиле**](-wia-iscanprofile.md) выполняется запись более чем одного процесса, то единственный процесс, который вызывает **Исканпрофиле:: Save** Last, является единственным процессом, изменения которого сохраняются.</span><span class="sxs-lookup"><span data-stu-id="7dc38-114">If more than one process writes to the [**IScanProfile**](-wia-iscanprofile.md) object, the one that calls **IScanProfile::Save** last is the only process whose changes are saved.</span></span>

<span data-ttu-id="7dc38-115">Метод **исканпрофиле:: Save** проверяет профиль перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="7dc38-115">The **IScanProfile::Save** method validates the profile before saving.</span></span> <span data-ttu-id="7dc38-116">Профиль всегда считается допустимым, если только Категория элемента (WIA) 2,0, связанная с профилем, является либо \_ \_ податчиком категории WIA, \_ либо \_ устройством подачи категорий WIA.</span><span class="sxs-lookup"><span data-stu-id="7dc38-116">The profile is always considered valid unless the category of the Windows Image Acquisition (WIA) 2.0 item associated with the profile is either WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER.</span></span> <span data-ttu-id="7dc38-117">Если категория имеет значение WIA категории " \_ \_ планшетный" или "WIA" \_ \_ , следующие свойства должны быть допустимы для элемента, если они содержатся в профиле:</span><span class="sxs-lookup"><span data-stu-id="7dc38-117">If the category is WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER, the following properties must be valid for the item, if the properties are contained in the profile:</span></span>

<span data-ttu-id="7dc38-118">\_яркость IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="7dc38-118">WIA\_IPS\_BRIGHTNESS</span></span>

<span data-ttu-id="7dc38-119">\_контрастные IP-адреса WIA \_</span><span class="sxs-lookup"><span data-stu-id="7dc38-119">WIA\_IPS\_CONTRAST</span></span>

<span data-ttu-id="7dc38-120">\_ \_ тип данных WIA IPA</span><span class="sxs-lookup"><span data-stu-id="7dc38-120">WIA\_IPA\_DATATYPE</span></span>

<span data-ttu-id="7dc38-121">\_ксрес IP-адресов WIA \_</span><span class="sxs-lookup"><span data-stu-id="7dc38-121">WIA\_IPS\_XRES</span></span>

<span data-ttu-id="7dc38-122">\_формат IPA \_ WIA</span><span class="sxs-lookup"><span data-stu-id="7dc38-122">WIA\_IPA\_FORMAT</span></span>

<span data-ttu-id="7dc38-123">Кроме того, если категория является \_ \_ податчиком категории WIA, \_ \_ свойство размера страницы IP-адресов WIA \_ должно быть допустимым, если оно есть в профиле.</span><span class="sxs-lookup"><span data-stu-id="7dc38-123">In addition, if the category is WIA\_CATEGORY\_FEEDER, the WIA\_IPS\_PAGE\_SIZE property must be valid, if it is present in the profile.</span></span> <span data-ttu-id="7dc38-124">Дополнительные сведения об этих свойствах см. в статье [**константы свойства элемента сканера WIA**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="7dc38-124">For more information about these properties, see [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc38-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7dc38-125">Requirements</span></span>



| <span data-ttu-id="7dc38-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7dc38-126">Requirement</span></span> | <span data-ttu-id="7dc38-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7dc38-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc38-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7dc38-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc38-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dc38-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7dc38-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7dc38-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc38-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7dc38-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dc38-132">Header</span><span class="sxs-lookup"><span data-stu-id="7dc38-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc38-133"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc38-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="7dc38-134">IDL</span><span class="sxs-lookup"><span data-stu-id="7dc38-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7dc38-135"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7dc38-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc38-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7dc38-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc38-137">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="7dc38-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="7dc38-138">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="7dc38-138">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





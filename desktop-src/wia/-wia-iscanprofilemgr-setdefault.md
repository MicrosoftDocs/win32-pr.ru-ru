---
description: Задает указанный профиль сканирования в качестве профиля по умолчанию.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Метод Исканпрофилемгр:: Сетдефаулт (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663395"
---
# <a name="iscanprofilemgrsetdefault-method"></a><span data-ttu-id="65413-103">Метод Исканпрофилемгр:: Сетдефаулт</span><span class="sxs-lookup"><span data-stu-id="65413-103">IScanProfileMgr::SetDefault method</span></span>

<span data-ttu-id="65413-104">Задает указанный профиль сканирования в качестве профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="65413-104">Sets the specified scan profile as the default profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="65413-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65413-105">Syntax</span></span>


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="65413-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="65413-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65413-107">*псканпрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65413-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65413-108">Тип: \**[**исканпрофиле**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="65413-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="65413-109">Указатель на профиль.</span><span class="sxs-lookup"><span data-stu-id="65413-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65413-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65413-110">Return value</span></span>

<span data-ttu-id="65413-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="65413-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="65413-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="65413-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65413-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65413-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65413-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65413-114">Remarks</span></span>

<span data-ttu-id="65413-115">Используйте метод **исканпрофилемгр:: сетдефаулт** , чтобы добавить `<Default>` элемент в профиль или удалить этот элемент из предыдущего профиля по умолчанию устройства.</span><span class="sxs-lookup"><span data-stu-id="65413-115">Use the **IScanProfileMgr::SetDefault** method to add a `<Default>` element to the profile or to remove that element from the device's previous default profile.</span></span>

<span data-ttu-id="65413-116">Используйте метод [**сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) для изменения профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="65413-116">Use the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method to change the default profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="65413-117">Требования</span><span class="sxs-lookup"><span data-stu-id="65413-117">Requirements</span></span>



| <span data-ttu-id="65413-118">Требование</span><span class="sxs-lookup"><span data-stu-id="65413-118">Requirement</span></span> | <span data-ttu-id="65413-119">Значение</span><span class="sxs-lookup"><span data-stu-id="65413-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="65413-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65413-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65413-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65413-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="65413-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65413-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65413-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65413-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65413-124">Header</span><span class="sxs-lookup"><span data-stu-id="65413-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65413-125"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="65413-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="65413-126">IDL</span><span class="sxs-lookup"><span data-stu-id="65413-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65413-127"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65413-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65413-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65413-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65413-129">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="65413-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="65413-130">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="65413-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





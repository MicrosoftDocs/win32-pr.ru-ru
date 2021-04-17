---
description: Задает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Метод Исканпрофиле:: Сетитем (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711257"
---
# <a name="iscanprofilesetitem-method"></a><span data-ttu-id="29542-103">Метод Исканпрофиле:: Сетитем</span><span class="sxs-lookup"><span data-stu-id="29542-103">IScanProfile::SetItem method</span></span>

<span data-ttu-id="29542-104">Задает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.</span><span class="sxs-lookup"><span data-stu-id="29542-104">Sets the GUID of the category of Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="29542-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29542-105">Syntax</span></span>


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="29542-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="29542-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29542-107">*гуидкатегори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29542-107">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29542-108">Тип: **GUID**</span><span class="sxs-lookup"><span data-stu-id="29542-108">Type: **GUID**</span></span>

<span data-ttu-id="29542-109">Идентификатор GUID категории элемента WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="29542-109">The GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="29542-110">Это должна быть одна из \_ \_ констант категории элемента WIA IPA \_ .</span><span class="sxs-lookup"><span data-stu-id="29542-110">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29542-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29542-111">Return value</span></span>

<span data-ttu-id="29542-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="29542-112">Type: **HRESULT**</span></span>

<span data-ttu-id="29542-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="29542-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="29542-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29542-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29542-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29542-115">Remarks</span></span>

<span data-ttu-id="29542-116">Пользователи могут изменить категорию с помощью метода [**сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="29542-116">Users can change the category with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="29542-117">Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="29542-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="29542-118">Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.</span><span class="sxs-lookup"><span data-stu-id="29542-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="29542-119">Требования</span><span class="sxs-lookup"><span data-stu-id="29542-119">Requirements</span></span>



| <span data-ttu-id="29542-120">Требование</span><span class="sxs-lookup"><span data-stu-id="29542-120">Requirement</span></span> | <span data-ttu-id="29542-121">Значение</span><span class="sxs-lookup"><span data-stu-id="29542-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="29542-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29542-122">Minimum supported client</span></span><br/> | <span data-ttu-id="29542-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29542-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="29542-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29542-124">Minimum supported server</span></span><br/> | <span data-ttu-id="29542-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29542-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29542-126">Header</span><span class="sxs-lookup"><span data-stu-id="29542-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="29542-127"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="29542-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="29542-128">IDL</span><span class="sxs-lookup"><span data-stu-id="29542-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29542-129"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="29542-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29542-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29542-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29542-131">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="29542-131">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="29542-132">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="29542-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





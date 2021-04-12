---
description: Отображает диалоговое окно, позволяющее пользователям создавать, изменять и удалять профили сканирования.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Метод Исканпрофилеуи:: Сканпрофиледиалог (Сканпрофилеуи. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264530"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a><span data-ttu-id="92ab2-103">Метод Исканпрофилеуи:: Сканпрофиледиалог</span><span class="sxs-lookup"><span data-stu-id="92ab2-103">IScanProfileUI::ScanProfileDialog method</span></span>

<span data-ttu-id="92ab2-104">Отображает диалоговое окно, позволяющее пользователям создавать, изменять и удалять профили сканирования.</span><span class="sxs-lookup"><span data-stu-id="92ab2-104">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span>

## <a name="syntax"></a><span data-ttu-id="92ab2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92ab2-105">Syntax</span></span>


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="92ab2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92ab2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92ab2-107">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92ab2-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92ab2-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="92ab2-108">Type: **HWND**</span></span>

<span data-ttu-id="92ab2-109">Маркер родительского окна, которому принадлежит диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="92ab2-109">The handle of the parent window that owns the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92ab2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92ab2-110">Return value</span></span>

<span data-ttu-id="92ab2-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="92ab2-111">Type: **HRESULT**</span></span>

<span data-ttu-id="92ab2-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="92ab2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92ab2-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="92ab2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="92ab2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92ab2-114">Remarks</span></span>

<span data-ttu-id="92ab2-115">Диалоговое окно является модальным; пользователь не может переключиться на родительское окно, пока диалоговое окно не закроется.</span><span class="sxs-lookup"><span data-stu-id="92ab2-115">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

<span data-ttu-id="92ab2-116">Значения `<ProfileName>` элемента и `<WiaItem>` элемента можно изменить в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="92ab2-116">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed in the dialog box.</span></span> <span data-ttu-id="92ab2-117">`<Default>`Элемент можно добавить или удалить.</span><span class="sxs-lookup"><span data-stu-id="92ab2-117">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="92ab2-118">Другие изменения профиля сканирования не могут быть сделаны в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="92ab2-118">No other changes to the scan profile can be made in the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="92ab2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="92ab2-119">Requirements</span></span>



| <span data-ttu-id="92ab2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="92ab2-120">Requirement</span></span> | <span data-ttu-id="92ab2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="92ab2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="92ab2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92ab2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92ab2-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92ab2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="92ab2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92ab2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92ab2-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92ab2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92ab2-126">Header</span><span class="sxs-lookup"><span data-stu-id="92ab2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92ab2-127"><dt>Сканпрофилеуи. h</dt></span><span class="sxs-lookup"><span data-stu-id="92ab2-127"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="92ab2-128">IDL</span><span class="sxs-lookup"><span data-stu-id="92ab2-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92ab2-129"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92ab2-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92ab2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92ab2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ab2-131">**исканпрофилеуи**</span><span class="sxs-lookup"><span data-stu-id="92ab2-131">**IScanProfileUI**</span></span>](-wia-iscanprofileui.md)
</dt> <dt>

[<span data-ttu-id="92ab2-132">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="92ab2-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





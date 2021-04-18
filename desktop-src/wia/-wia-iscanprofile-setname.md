---
description: Задает понятное имя профиля.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'Метод Исканпрофиле:: SetName (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711967"
---
# <a name="iscanprofilesetname-method"></a><span data-ttu-id="f790c-103">Метод Исканпрофиле:: SetName</span><span class="sxs-lookup"><span data-stu-id="f790c-103">IScanProfile::SetName method</span></span>

<span data-ttu-id="f790c-104">Задает понятное имя профиля.</span><span class="sxs-lookup"><span data-stu-id="f790c-104">Sets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f790c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f790c-105">Syntax</span></span>


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a><span data-ttu-id="f790c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f790c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f790c-107">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f790c-107">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f790c-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f790c-108">Type: **BSTR**</span></span>

<span data-ttu-id="f790c-109">Понятное имя профиля.</span><span class="sxs-lookup"><span data-stu-id="f790c-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f790c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f790c-110">Return value</span></span>

<span data-ttu-id="f790c-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f790c-111">Type: **HRESULT**</span></span>

<span data-ttu-id="f790c-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f790c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f790c-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f790c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f790c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f790c-114">Remarks</span></span>

<span data-ttu-id="f790c-115">Этот метод является обязательным, поскольку идентификатор GUID профиля не может использоваться для вывода профиля сканирования пользователю.</span><span class="sxs-lookup"><span data-stu-id="f790c-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

<span data-ttu-id="f790c-116">Пользователь может изменить понятное имя профиля с помощью метода [**сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="f790c-116">A user can change the friendly name of a profile with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="f790c-117">Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="f790c-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="f790c-118">Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.</span><span class="sxs-lookup"><span data-stu-id="f790c-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="f790c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f790c-119">Requirements</span></span>



| <span data-ttu-id="f790c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f790c-120">Requirement</span></span> | <span data-ttu-id="f790c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f790c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f790c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f790c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f790c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f790c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f790c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f790c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f790c-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f790c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f790c-126">Header</span><span class="sxs-lookup"><span data-stu-id="f790c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f790c-127"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="f790c-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="f790c-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f790c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f790c-129"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f790c-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



 

 





---
description: Метод Двдадм. ConfirmPassword проверяет, соответствует ли указанный пароль ранее сохраненному паролю.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Метод ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668655"
---
# <a name="confirmpassword-method"></a><span data-ttu-id="fcabe-103">Метод ConfirmPassword</span><span class="sxs-lookup"><span data-stu-id="fcabe-103">ConfirmPassword Method</span></span>

> [!Note]  
> <span data-ttu-id="fcabe-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fcabe-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fcabe-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="fcabe-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fcabe-106">`DVDAdm.ConfirmPassword`Метод проверяет, соответствует ли указанный пароль ранее сохраненному паролю.</span><span class="sxs-lookup"><span data-stu-id="fcabe-106">The `DVDAdm.ConfirmPassword` method tests whether the specified password matches the previously saved password.</span></span>

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="fcabe-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fcabe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcabe-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*</span><span class="sxs-lookup"><span data-stu-id="fcabe-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="fcabe-109">Указывает имя пользователя в виде строки.</span><span class="sxs-lookup"><span data-stu-id="fcabe-109">Specifies the user's name as a String.</span></span>

</dd> <dt>

<span data-ttu-id="fcabe-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*</span><span class="sxs-lookup"><span data-stu-id="fcabe-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="fcabe-111">Указывает новый пароль в виде строки.</span><span class="sxs-lookup"><span data-stu-id="fcabe-111">Specifies the new password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcabe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fcabe-112">Return Value</span></span>

<span data-ttu-id="fcabe-113">Возвращает значение true, если указанный пароль совпадает с существующим паролем, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fcabe-113">Returns true if the specified password matches the existing password, false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcabe-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcabe-114">Remarks</span></span>

<span data-ttu-id="fcabe-115">В настоящее время параметр *сусернаме* игнорируется на этом и всех связанных методах.</span><span class="sxs-lookup"><span data-stu-id="fcabe-115">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcabe-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fcabe-116">Requirements</span></span>



| <span data-ttu-id="fcabe-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fcabe-117">Requirement</span></span> | <span data-ttu-id="fcabe-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fcabe-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcabe-119">Header</span><span class="sxs-lookup"><span data-stu-id="fcabe-119">Header</span></span><br/> | <dl> <span data-ttu-id="fcabe-120"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcabe-120"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcabe-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcabe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcabe-122">**ChangePassword;**</span><span class="sxs-lookup"><span data-stu-id="fcabe-122">**ChangePassword**</span></span>](changepassword-method.md)
</dt> <dt>

[<span data-ttu-id="fcabe-123">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="fcabe-123">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 





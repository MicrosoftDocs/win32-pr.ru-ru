---
description: Метод Двдадм. ChangePassword сохраняет новый пароль приложения в реестре.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: Метод ChangePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494526"
---
# <a name="changepassword-method"></a><span data-ttu-id="c638a-103">Метод ChangePassword</span><span class="sxs-lookup"><span data-stu-id="c638a-103">ChangePassword Method</span></span>

> [!Note]  
> <span data-ttu-id="c638a-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c638a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c638a-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="c638a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c638a-106">`DVDAdm.ChangePassword`Метод сохраняет новый пароль приложения в реестре.</span><span class="sxs-lookup"><span data-stu-id="c638a-106">The `DVDAdm.ChangePassword` method saves a new application password in the registry.</span></span>

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a><span data-ttu-id="c638a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c638a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c638a-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*</span><span class="sxs-lookup"><span data-stu-id="c638a-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="c638a-109">Указывает имя входа текущего пользователя в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c638a-109">Specifies the current user's logon name as a String.</span></span> <span data-ttu-id="c638a-110">Объект Мсдвдадм игнорирует этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c638a-110">The MSDVDAdm object ignores this parameter.</span></span> <span data-ttu-id="c638a-111">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="c638a-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c638a-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Данного*</span><span class="sxs-lookup"><span data-stu-id="c638a-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*sOld*</span></span>
</dt> <dd>

<span data-ttu-id="c638a-113">Указывает старый пароль пользователя в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c638a-113">Specifies the user's old password as a String.</span></span>

</dd> <dt>

<span data-ttu-id="c638a-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*снев*</span><span class="sxs-lookup"><span data-stu-id="c638a-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span></span>
</dt> <dd>

<span data-ttu-id="c638a-115">Указывает новый пароль пользователя в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c638a-115">Specifies the user's new password as a String.</span></span> <span data-ttu-id="c638a-116">не может быть пустой строкой;</span><span class="sxs-lookup"><span data-stu-id="c638a-116">Cannot be an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c638a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c638a-117">Return Value</span></span>

<span data-ttu-id="c638a-118">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c638a-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c638a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c638a-119">Remarks</span></span>

<span data-ttu-id="c638a-120">В настоящее время параметр *сусернаме* игнорируется на этом и всех связанных методах.</span><span class="sxs-lookup"><span data-stu-id="c638a-120">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span> <span data-ttu-id="c638a-121">Это означает, что кто угодно знает, что пароль может установить родительский уровень.</span><span class="sxs-lookup"><span data-stu-id="c638a-121">This means that whoever knows the password can set the parental level.</span></span> <span data-ttu-id="c638a-122">Для приложения существует только один пароль и один родительский уровень.</span><span class="sxs-lookup"><span data-stu-id="c638a-122">There is only one password and one parental level for the application.</span></span> <span data-ttu-id="c638a-123">Не поддерживается отдельное имя пользователя для входа в систему или управление паролями.</span><span class="sxs-lookup"><span data-stu-id="c638a-123">There is no support for individual user logon names or multiple password management.</span></span> <span data-ttu-id="c638a-124">Чтобы применить уровни родительского управления, родительские элементы должны задать пароль, а затем задать уровень родительского уровня, соответствующий младшим членам группы родственников.</span><span class="sxs-lookup"><span data-stu-id="c638a-124">To enforce parental management levels, parents should set the password and then set the parental level appropriate for younger members of the group of relatives.</span></span> <span data-ttu-id="c638a-125">Когда родители хотят просмотреть диск с содержимым для взрослых, он может изменить уровень, а затем снова изменить его после завершения просмотра.</span><span class="sxs-lookup"><span data-stu-id="c638a-125">When parents want to view a disc with adult-rated content, they can change the level, and then change it back when they are done viewing.</span></span> <span data-ttu-id="c638a-126">Пока дочерние элементы не узнают пароль, они могут просматривать только содержимое на уровне, установленном для них.</span><span class="sxs-lookup"><span data-stu-id="c638a-126">As long as the children do not know the password, they can only watch content at or below the level set for them.</span></span>

## <a name="see-also"></a><span data-ttu-id="c638a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c638a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c638a-128">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="c638a-128">**ConfirmPassword**</span></span>](confirmpassword-method.md)
</dt> <dt>

[<span data-ttu-id="c638a-129">Объект Мсдвдадм</span><span class="sxs-lookup"><span data-stu-id="c638a-129">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




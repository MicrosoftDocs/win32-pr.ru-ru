---
title: Настраиваемые свойства пользователя WinNT
description: Поставщик WinNT предоставляет доступ к следующим пользовательским свойствам для класса User. Доступ к ним можно получить с помощью методов IADs. Get и IADs. постановки. Дополнительные сведения см. в разделе \_ Структура сведений о пользователе \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- Интерфейсы ADSI настраиваемых свойств пользователя WinNT
- Службы WinNT Provider ADSI, объект User, пользовательские свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987886"
---
# <a name="winnt-custom-user-properties"></a><span data-ttu-id="04d7a-107">Настраиваемые свойства пользователя WinNT</span><span class="sxs-lookup"><span data-stu-id="04d7a-107">WinNT Custom User Properties</span></span>

<span data-ttu-id="04d7a-108">Поставщик WinNT предоставляет доступ к следующим пользовательским свойствам для класса User.</span><span class="sxs-lookup"><span data-stu-id="04d7a-108">The WinNT provider makes available the following custom properties for the User class.</span></span> <span data-ttu-id="04d7a-109">Доступ к ним можно получить с помощью методов [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. постановки**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="04d7a-109">They may be accessed through the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) methods.</span></span> <span data-ttu-id="04d7a-110">Дополнительные сведения см. в разделе [**Структура \_ сведений о пользователе \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .</span><span class="sxs-lookup"><span data-stu-id="04d7a-110">For more information, see the [**USER\_INFO\_3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) structure.</span></span>



| <span data-ttu-id="04d7a-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="04d7a-111">Property</span></span>            | <span data-ttu-id="04d7a-112">Тип</span><span class="sxs-lookup"><span data-stu-id="04d7a-112">Type</span></span>         | <span data-ttu-id="04d7a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="04d7a-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d7a-114">**хомедирдриве**</span><span class="sxs-lookup"><span data-stu-id="04d7a-114">**HomeDirDrive**</span></span>    | <span data-ttu-id="04d7a-115">Строка</span><span class="sxs-lookup"><span data-stu-id="04d7a-115">String</span></span>       | <span data-ttu-id="04d7a-116">Диск домашнего каталога пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d7a-116">Home Directory Drive of the user.</span></span> <span data-ttu-id="04d7a-117">Это указатель на строку в Юникоде, указывающую путь к домашнему каталогу.</span><span class="sxs-lookup"><span data-stu-id="04d7a-117">This is a pointer to a Unicode string that specifies the path of the home directory.</span></span> <span data-ttu-id="04d7a-118">Строка может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="04d7a-118">The string can be **null**.</span></span> <span data-ttu-id="04d7a-119">См. пример в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="04d7a-119">See example in this topic.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="04d7a-120">**ObjectSID**</span><span class="sxs-lookup"><span data-stu-id="04d7a-120">**ObjectSID**</span></span>       | <span data-ttu-id="04d7a-121">Строка октета</span><span class="sxs-lookup"><span data-stu-id="04d7a-121">Octet String</span></span> | <span data-ttu-id="04d7a-122">Идентификатор безопасности объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d7a-122">Object SID of the user.</span></span> <span data-ttu-id="04d7a-123">Пример получения идентификатора безопасности объекта с помощью поставщика WinNT см. в разделе [SID объекта (поставщик WinNT)](object-sid.md) .</span><span class="sxs-lookup"><span data-stu-id="04d7a-123">For an example of how to retrieve the Object SID using the WinNT Provider, see [Object SID (WinNT Provider)](object-sid.md)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="04d7a-124">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="04d7a-124">**Parameters**</span></span>      | <span data-ttu-id="04d7a-125">Строка</span><span class="sxs-lookup"><span data-stu-id="04d7a-125">String</span></span>       | <span data-ttu-id="04d7a-126">Параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d7a-126">Parameters of the user.</span></span> <span data-ttu-id="04d7a-127">Указывает на строку в Юникоде, которая задается не для использования приложениями.</span><span class="sxs-lookup"><span data-stu-id="04d7a-127">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="04d7a-128">Эта строка может быть пустой строкой или содержать любое число символов перед завершающим нулевым символом.</span><span class="sxs-lookup"><span data-stu-id="04d7a-128">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="04d7a-129">Продукты Майкрософт используют этот элемент для хранения данных конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d7a-129">Microsoft products use this member to store user configuration data.</span></span> <span data-ttu-id="04d7a-130">Это свойство может быть изменено приложением только во время установки.</span><span class="sxs-lookup"><span data-stu-id="04d7a-130">This property can only be modified by an application during installation.</span></span> |
| <span data-ttu-id="04d7a-131">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="04d7a-131">**PasswordAge**</span></span>     | <span data-ttu-id="04d7a-132">Время</span><span class="sxs-lookup"><span data-stu-id="04d7a-132">Time</span></span>         | <span data-ttu-id="04d7a-133">Продолжительность использования пароля.</span><span class="sxs-lookup"><span data-stu-id="04d7a-133">Time duration of the password in use.</span></span> <span data-ttu-id="04d7a-134">Это свойство указывает число секунд, прошедших с момента последнего изменения пароля.</span><span class="sxs-lookup"><span data-stu-id="04d7a-134">This property indicates the number of seconds that have elapsed since the password was last changed.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="04d7a-135">**пассвордекспиред**</span><span class="sxs-lookup"><span data-stu-id="04d7a-135">**PasswordExpired**</span></span> | <span data-ttu-id="04d7a-136">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="04d7a-136">Integer</span></span>      | <span data-ttu-id="04d7a-137">Сообщает, когда истек срок действия пароля.</span><span class="sxs-lookup"><span data-stu-id="04d7a-137">Tells when the password was expired.</span></span> <span data-ttu-id="04d7a-138">При использовании Get возвращается ноль, если срок действия пароля не истек или он не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="04d7a-138">When you use Get, it will return zero is the password has not expired, or nonzero if it has expired.</span></span> <span data-ttu-id="04d7a-139">См. пример в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="04d7a-139">See example in this topic.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="04d7a-140">**примариграупид**</span><span class="sxs-lookup"><span data-stu-id="04d7a-140">**PrimaryGroupID**</span></span>  | <span data-ttu-id="04d7a-141">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="04d7a-141">Integer</span></span>      | <span data-ttu-id="04d7a-142">Идентификатор основной группы пользователей, например идентификатор группы пользователей домена.</span><span class="sxs-lookup"><span data-stu-id="04d7a-142">User's primary group ID, for example, domain user group ID.</span></span> <span data-ttu-id="04d7a-143">См. пример в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="04d7a-143">See example in this topic.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="04d7a-144">**усерфлагс**</span><span class="sxs-lookup"><span data-stu-id="04d7a-144">**UserFlags**</span></span>       | <span data-ttu-id="04d7a-145">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="04d7a-145">Integer</span></span>      | <span data-ttu-id="04d7a-146">Флаг пользователя, определенный [**в \_ \_ \_ перечислении флагов пользователей ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span><span class="sxs-lookup"><span data-stu-id="04d7a-146">User Flag defined in [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span></span> <span data-ttu-id="04d7a-147">Пример использования Усерфлагс см. в разделе [срок действия пароля никогда не истекает (поставщик WinNT)](winnt-password-never-expires.md) .</span><span class="sxs-lookup"><span data-stu-id="04d7a-147">For an example of how to use UserFlags, see [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)</span></span>                                                                                                                                                             |



 

<span data-ttu-id="04d7a-148">В этом примере показано, как задать каталог домашнего диска пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d7a-148">This example shows how to set a user's Home Drive Directory.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



<span data-ttu-id="04d7a-149">В этом примере показано, как использовать Пассвордекспиред для принудительного изменения пароля пользователем при следующем входе в систему.</span><span class="sxs-lookup"><span data-stu-id="04d7a-149">This example shows how to use PasswordExpired to force a user to change the password at the next logon.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



<span data-ttu-id="04d7a-150">В этом примере показано, как получить основную группу пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d7a-150">This example shows how to get the user's primary group.</span></span>


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 
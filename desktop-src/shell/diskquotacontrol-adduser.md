---
description: Назначает для нового пользователя квоту диска, не используемую по умолчанию.
title: Дисккуотаконтрол. AddUser, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.AddUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: de20d016-83da-42ac-962f-86faf9b25419
ms.openlocfilehash: e91bfee0cf491d7191d64bdec6ed7593e10654ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540474"
---
# <a name="diskquotacontroladduser-method"></a><span data-ttu-id="b9aa9-103">Дисккуотаконтрол. AddUser, метод</span><span class="sxs-lookup"><span data-stu-id="b9aa9-103">DiskQuotaControl.AddUser method</span></span>

<span data-ttu-id="b9aa9-104">Назначает для нового пользователя квоту диска, не используемую по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-104">Assigns a nondefault disk quota to a new user.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9aa9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9aa9-105">Syntax</span></span>


```JScript
objRetVal = DiskQuotaControl.AddUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="b9aa9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9aa9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9aa9-107">*слогоннаме*</span><span class="sxs-lookup"><span data-stu-id="b9aa9-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="b9aa9-108">Тип: **char**</span><span class="sxs-lookup"><span data-stu-id="b9aa9-108">Type: **CHAR**</span></span>

<span data-ttu-id="b9aa9-109">Строковое значение, содержащее имя входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-109">A string value that contains the user's logon name.</span></span> <span data-ttu-id="b9aa9-110">Используйте свойство [**усернамересолутион**](diskquotacontrol-usernameresolution.md) , чтобы указать способ разрешения имени.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-110">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to specify how the name is to be resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9aa9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9aa9-111">Return value</span></span>

<span data-ttu-id="b9aa9-112">Тип: **объект**</span><span class="sxs-lookup"><span data-stu-id="b9aa9-112">Type: **Object**</span></span>

<span data-ttu-id="b9aa9-113">Возвращает выражение объекта, результатом которого является объект пользователя [**дидисккуотаусер**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b9aa9-113">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9aa9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9aa9-114">Remarks</span></span>

<span data-ttu-id="b9aa9-115">При первой записи пользователя в том файловая система NTFS автоматически создает запись квоты пользователя.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-115">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="b9aa9-116">Записям, созданным таким образом, назначаются порог предупреждения по умолчанию и значения фиксированной квоты для тома.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-116">Entries that are created in this way are assigned the default warning threshold and hard quota limit values for the volume.</span></span> <span data-ttu-id="b9aa9-117">Этот метод позволяет создать запись квоты пользователя до того, как пользователь запишет данные в том.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-117">This method allows you to create a user quota entry before a user writes information to the volume.</span></span> <span data-ttu-id="b9aa9-118">Он возвращает объект [**дидисккуотаусер**](didiskquotauser-object.md) , который можно использовать для назначения порога предупреждения или значения квоты, отличающегося от параметров по умолчанию для тома.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-118">It returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to assign a warning threshold or quota limit value that differs from the default settings for the volume.</span></span>

<span data-ttu-id="b9aa9-119">Если пользователь уже существует, Новая запись не создается.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-119">If the user already exists, no new entry is created.</span></span> <span data-ttu-id="b9aa9-120">Метод возвращает объект [**дидисккуотаусер**](didiskquotauser-object.md) , связанный с существующей записью.</span><span class="sxs-lookup"><span data-stu-id="b9aa9-120">The method returns the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the existing entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9aa9-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b9aa9-121">Requirements</span></span>



| <span data-ttu-id="b9aa9-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b9aa9-122">Requirement</span></span> | <span data-ttu-id="b9aa9-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b9aa9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9aa9-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9aa9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b9aa9-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9aa9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9aa9-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9aa9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b9aa9-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9aa9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b9aa9-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b9aa9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9aa9-129"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b9aa9-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9aa9-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9aa9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9aa9-131">**дефаулткуоталимит**</span><span class="sxs-lookup"><span data-stu-id="b9aa9-131">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="b9aa9-132">**дефаулткуотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="b9aa9-132">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="b9aa9-133">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="b9aa9-133">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 





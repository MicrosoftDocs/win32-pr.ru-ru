---
title: Свойство ConnectionOptions. Password (Всмандисп. h)
description: Задает пароль локальной или доменной учетной записи на удаленном компьютере. Это свойство определяет пароль для проверки подлинности.
ms.assetid: 61ba54b6-7da0-423e-b5b2-c4dd8aacd042
ms.tgt_platform: multiple
keywords:
- Свойство пароля служба удаленного управления Windows
- Свойство Password служба удаленного управления Windows, объект ConnectionOptions
- Служба удаленного управления Windows объекта ConnectionOptions, свойство Password
topic_type:
- apiref
api_name:
- ConnectionOptions.Password
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4d553bf3f2a0a245e358e09a89eb1c00751e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136503"
---
# <a name="connectionoptionspassword-property"></a><span data-ttu-id="9b25f-107">ConnectionOptions. Password, свойство</span><span class="sxs-lookup"><span data-stu-id="9b25f-107">ConnectionOptions.Password property</span></span>

<span data-ttu-id="9b25f-108">Задает пароль локальной или доменной учетной записи на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9b25f-108">Sets the password of a local or a domain account on the remote computer.</span></span> <span data-ttu-id="9b25f-109">Это свойство определяет пароль для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9b25f-109">This property determines the password for authentication.</span></span> <span data-ttu-id="9b25f-110">Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="9b25f-110">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

<span data-ttu-id="9b25f-111">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9b25f-111">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b25f-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b25f-112">Syntax</span></span>


```VB
ConnectionOptions.Password As String
```



## <a name="property-value"></a><span data-ttu-id="9b25f-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9b25f-113">Property value</span></span>

<span data-ttu-id="9b25f-114">Строка, содержащая пароль локальной или доменной учетной записи на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9b25f-114">String that contains the password of a local or a domain account on the remote computer.</span></span>

<span data-ttu-id="9b25f-115">Если значение не указано, а флаг **всманфлагкредусернамепассворд** не установлен, используется пароль учетной записи, в которой работает скрипт.</span><span class="sxs-lookup"><span data-stu-id="9b25f-115">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is not set, the password of the account that is running the script is used.</span></span>

<span data-ttu-id="9b25f-116">Если значение не указано и установлен флаг **всманфлагкредусернамепассворд** , сценарий предлагает пользователю ввести пароль (и имя пользователя, если оно не указано).</span><span class="sxs-lookup"><span data-stu-id="9b25f-116">If no value is supplied and the **WSManFlagCredUsernamePassword** flag is set, the script prompts the user to enter the password (and the user name, if this is not supplied).</span></span> <span data-ttu-id="9b25f-117">Если допустимое имя пользователя и пароль не указаны, возвращается ошибка отказа в доступе.</span><span class="sxs-lookup"><span data-stu-id="9b25f-117">If a valid user name and password are not entered, then an access denied error is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b25f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b25f-118">Remarks</span></span>

<span data-ttu-id="9b25f-119">Имейте в виду, что вы не можете получить пароль.</span><span class="sxs-lookup"><span data-stu-id="9b25f-119">Be aware that you cannot retrieve the password.</span></span> <span data-ttu-id="9b25f-120">Пароль можно задать только с помощью этого свойства.</span><span class="sxs-lookup"><span data-stu-id="9b25f-120">The password can only be set with this property.</span></span>

<span data-ttu-id="9b25f-121">Если вы создаете объект [**ConnectionOptions**](connectionoptions.md) и используете имя пользователя и пароль для подключения к служба удаленного управления Windows, установите флаг **Всманфлагкредусернамепассворд** для вызова [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="9b25f-121">If you create a [**ConnectionOptions**](connectionoptions.md) object and use a user name and password to connect to Windows Remote Management, then the **WSManFlagCredUserNamePassword** flag should be set on the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

<span data-ttu-id="9b25f-122">Дополнительные сведения о настройке паролей см. в разделе "Примечания" в [**ConnectionOptions**](connectionoptions.md).</span><span class="sxs-lookup"><span data-stu-id="9b25f-122">For more information about setting passwords, see the Remarks section in [**ConnectionOptions**](connectionoptions.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9b25f-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="9b25f-123">Examples</span></span>

<span data-ttu-id="9b25f-124">В следующем примере кода создается объект [**ConnectionOptions**](connectionoptions.md) и задается **пароль**.</span><span class="sxs-lookup"><span data-stu-id="9b25f-124">The following code example creates a [**ConnectionOptions**](connectionoptions.md) object and sets the **Password**.</span></span>


```VB
' Create a WSMan object. 
Set objWsman = CreateObject( "WSMAN.Automation" )
' Create a ConnectionOptions object
Set objOptions = objWSMan.CreateConnectionOptions
objOptions.Password = "<password>"
```



## <a name="requirements"></a><span data-ttu-id="9b25f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9b25f-125">Requirements</span></span>



| <span data-ttu-id="9b25f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9b25f-126">Requirement</span></span> | <span data-ttu-id="9b25f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9b25f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b25f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b25f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9b25f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b25f-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9b25f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b25f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9b25f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b25f-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9b25f-132">Header</span><span class="sxs-lookup"><span data-stu-id="9b25f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b25f-133"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b25f-133"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b25f-134">IDL</span><span class="sxs-lookup"><span data-stu-id="9b25f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b25f-135"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b25f-135"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9b25f-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b25f-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b25f-137"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b25f-137"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b25f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9b25f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b25f-139"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b25f-139"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b25f-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b25f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b25f-141">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="9b25f-141">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 






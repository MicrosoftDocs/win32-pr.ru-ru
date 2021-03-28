---
description: Позволяет клиенту управлять параметрами дисковой квоты на глобальные тома NTFS. Этот объект делает необходимые функции интерфейса Дидисккуотаусер доступными для создания сценариев и приложений на основе Microsoft Visual Basic.
title: Объект Дидисккуотаусер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: 5699ad9d15b0fa31c92f7d88df194f9012fa679d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984276"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="d991c-104">Объект Дидисккуотаусер</span><span class="sxs-lookup"><span data-stu-id="d991c-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="d991c-105">Позволяет клиенту управлять параметрами дисковой квоты на глобальные тома NTFS.</span><span class="sxs-lookup"><span data-stu-id="d991c-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="d991c-106">Этот объект делает необходимые функции интерфейса **дидисккуотаусер** доступными для создания сценариев и приложений на основе Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d991c-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="d991c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d991c-107">Members</span></span>

<span data-ttu-id="d991c-108">Объект **дидисккуотаусер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d991c-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="d991c-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d991c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d991c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d991c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d991c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d991c-111">Methods</span></span>

<span data-ttu-id="d991c-112">Объект **дидисккуотаусер** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="d991c-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="d991c-113">Метод</span><span class="sxs-lookup"><span data-stu-id="d991c-113">Method</span></span>                                           | <span data-ttu-id="d991c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d991c-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="d991c-115">**Недействительным**</span><span class="sxs-lookup"><span data-stu-id="d991c-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="d991c-116">Очищает кэшированные данные пользователя объекта.</span><span class="sxs-lookup"><span data-stu-id="d991c-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d991c-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="d991c-117">Properties</span></span>

<span data-ttu-id="d991c-118">Объект **дидисккуотаусер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d991c-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="d991c-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="d991c-119">Property</span></span>                                                                        | <span data-ttu-id="d991c-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d991c-120">Access type</span></span>           | <span data-ttu-id="d991c-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d991c-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d991c-122">**аккаунтконтаинернаме**</span><span class="sxs-lookup"><span data-stu-id="d991c-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="d991c-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-123">Read-only</span></span><br/>  | <span data-ttu-id="d991c-124">Возвращает имя контейнера учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="d991c-125">**аккаунтстатус**</span><span class="sxs-lookup"><span data-stu-id="d991c-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="d991c-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-126">Read-only</span></span><br/>  | <span data-ttu-id="d991c-127">Возвращает состояние учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="d991c-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d991c-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="d991c-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-129">Read-only</span></span><br/>  | <span data-ttu-id="d991c-130">Возвращает отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="d991c-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="d991c-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="d991c-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-132">Read-only</span></span><br/>  | <span data-ttu-id="d991c-133">Возвращает идентификатор, который однозначно идентифицирует пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="d991c-134">**логоннаме**</span><span class="sxs-lookup"><span data-stu-id="d991c-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="d991c-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-135">Read-only</span></span><br/>  | <span data-ttu-id="d991c-136">Возвращает имя учетной записи входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="d991c-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d991c-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="d991c-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d991c-138">Read/write</span></span><br/> | <span data-ttu-id="d991c-139">Задает или возвращает текущую [**квоту**](diskquotacontrol-object.md)пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="d991c-140">**куоталимиттекст**</span><span class="sxs-lookup"><span data-stu-id="d991c-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="d991c-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-141">Read-only</span></span><br/>  | <span data-ttu-id="d991c-142">Возвращает текущую [**предельную квоту**](diskquotacontrol-object.md) пользователя в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="d991c-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="d991c-143">**куотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="d991c-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="d991c-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d991c-144">Read/write</span></span><br/> | <span data-ttu-id="d991c-145">Задает или возвращает порог предупреждения пользователя в байтах.</span><span class="sxs-lookup"><span data-stu-id="d991c-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="d991c-146">**куотасрешолдтекст**</span><span class="sxs-lookup"><span data-stu-id="d991c-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="d991c-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-147">Read-only</span></span><br/>  | <span data-ttu-id="d991c-148">Возвращает пороговое значение предупреждения пользователя в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="d991c-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="d991c-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="d991c-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="d991c-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-150">Read-only</span></span><br/>  | <span data-ttu-id="d991c-151">Возвращает текущее использование диска пользователем в байтах.</span><span class="sxs-lookup"><span data-stu-id="d991c-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="d991c-152">**куотауседтекст**</span><span class="sxs-lookup"><span data-stu-id="d991c-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="d991c-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d991c-153">Read-only</span></span><br/>  | <span data-ttu-id="d991c-154">Возвращает текущий объем использования диска пользователем в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="d991c-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="d991c-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="d991c-155">Remarks</span></span>

<span data-ttu-id="d991c-156">Каждый пользователь на томе, управляемом объектом [**дисккуотаконтрол**](diskquotacontrol-object.md) , имеет связанный с ним объект **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="d991c-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="d991c-157">Этот объект позволяет клиенту управлять параметрами отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d991c-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="d991c-158">Существует несколько способов получить объект **дидисккуотаусер** пользователя:</span><span class="sxs-lookup"><span data-stu-id="d991c-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="d991c-159">Объекты **дидисккуотаусер** для всех пользователей с квотами на томе предоставляются в виде коллекции, и их можно перечислить.</span><span class="sxs-lookup"><span data-stu-id="d991c-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="d991c-160">Ниже приведено обсуждение того, как перечислить объекты **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="d991c-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="d991c-161">При добавлении нового пользователя метод [**adduser**](diskquotacontrol-adduser.md) возвращает объект пользователя **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="d991c-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="d991c-162">Если у вас есть имя пользователя, метод [**финдусер**](diskquotacontrol-finduser.md) возвращает объект **дидисккуотаусер** пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="d991c-163">Перечисление пользователей дисковой квоты</span><span class="sxs-lookup"><span data-stu-id="d991c-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="d991c-164">Объекты **дидисккуотаусер** для всех пользователей с квотой на том предоставляются в виде коллекции.</span><span class="sxs-lookup"><span data-stu-id="d991c-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="d991c-165">Объект [**дисккуотаконтрол**](diskquotacontrol-object.md) экспортирует стандартный метод перечислителя, позволяющий перечислить коллекцию объектов **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="d991c-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="d991c-166">Следующая процедура показывает, как выполнить перечисление с помощью Microsoft JScript (совместимой с спецификацией языка ECMA 262).</span><span class="sxs-lookup"><span data-stu-id="d991c-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="d991c-167">Аналогичную процедуру можно использовать с Visual Basic или Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="d991c-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="d991c-168">Создайте новый объект [**дисккуотаконтрол**](diskquotacontrol-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d991c-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="d991c-169">Инициализируйте его с помощью [**Initialize**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="d991c-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="d991c-170">Создайте новый объект **перечислителя** JScript.</span><span class="sxs-lookup"><span data-stu-id="d991c-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="d991c-171">Используйте цикл **for** для перечисления объектов **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="d991c-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="d991c-172">Нет необходимости задавать начальное значение.</span><span class="sxs-lookup"><span data-stu-id="d991c-172">There is no need to set a starting value.</span></span> <span data-ttu-id="d991c-173">Метод **MoveNext** объекта перечислителя уведомляет метод **Item** , чтобы вернуть следующий объект **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="d991c-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="d991c-174">Метод **atEnd** возвращает **значение false** , если достигнут конец списка.</span><span class="sxs-lookup"><span data-stu-id="d991c-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="d991c-175">При необходимости используйте объект **дидисккуотаусер** , возвращенный методом **элемента** перечислителя, для получения или задания одного или нескольких свойств квоты диска связанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="d991c-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="d991c-176">В следующем фрагменте кода показано, как перечислить объекты **дидисккуотаусер** с помощью JScript.</span><span class="sxs-lookup"><span data-stu-id="d991c-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="d991c-177">Аргумент **\_ метки тома** , передаваемый функции **енумусерс** , представляет собой строковое значение, содержащее метку тома, например "C: \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="d991c-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a><span data-ttu-id="d991c-178">Требования</span><span class="sxs-lookup"><span data-stu-id="d991c-178">Requirements</span></span>



| <span data-ttu-id="d991c-179">Требование</span><span class="sxs-lookup"><span data-stu-id="d991c-179">Requirement</span></span> | <span data-ttu-id="d991c-180">Значение</span><span class="sxs-lookup"><span data-stu-id="d991c-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d991c-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d991c-181">Minimum supported client</span></span><br/> | <span data-ttu-id="d991c-182">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d991c-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d991c-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d991c-183">Minimum supported server</span></span><br/> | <span data-ttu-id="d991c-184">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d991c-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d991c-185">DLL</span><span class="sxs-lookup"><span data-stu-id="d991c-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d991c-186"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d991c-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d991c-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d991c-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d991c-188">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="d991c-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 





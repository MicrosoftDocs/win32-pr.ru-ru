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
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843245"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="df4df-104">Объект Дидисккуотаусер</span><span class="sxs-lookup"><span data-stu-id="df4df-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="df4df-105">Позволяет клиенту управлять параметрами дисковой квоты на глобальные тома NTFS.</span><span class="sxs-lookup"><span data-stu-id="df4df-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="df4df-106">Этот объект делает необходимые функции интерфейса **дидисккуотаусер** доступными для создания сценариев и приложений на основе Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="df4df-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="df4df-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="df4df-107">Members</span></span>

<span data-ttu-id="df4df-108">Объект **дидисккуотаусер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="df4df-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="df4df-109">Методы</span><span class="sxs-lookup"><span data-stu-id="df4df-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="df4df-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="df4df-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df4df-111">Методы</span><span class="sxs-lookup"><span data-stu-id="df4df-111">Methods</span></span>

<span data-ttu-id="df4df-112">Объект **дидисккуотаусер** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="df4df-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="df4df-113">Метод</span><span class="sxs-lookup"><span data-stu-id="df4df-113">Method</span></span>                                           | <span data-ttu-id="df4df-114">Описание</span><span class="sxs-lookup"><span data-stu-id="df4df-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="df4df-115">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="df4df-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="df4df-116">Очищает кэшированные данные пользователя объекта.</span><span class="sxs-lookup"><span data-stu-id="df4df-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df4df-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="df4df-117">Properties</span></span>

<span data-ttu-id="df4df-118">Объект **дидисккуотаусер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="df4df-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="df4df-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="df4df-119">Property</span></span>                                                                        | <span data-ttu-id="df4df-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="df4df-120">Access type</span></span>           | <span data-ttu-id="df4df-121">Описание</span><span class="sxs-lookup"><span data-stu-id="df4df-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df4df-122">**аккаунтконтаинернаме**</span><span class="sxs-lookup"><span data-stu-id="df4df-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="df4df-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-123">Read-only</span></span><br/>  | <span data-ttu-id="df4df-124">Возвращает имя контейнера учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="df4df-125">**аккаунтстатус**</span><span class="sxs-lookup"><span data-stu-id="df4df-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="df4df-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-126">Read-only</span></span><br/>  | <span data-ttu-id="df4df-127">Возвращает состояние учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="df4df-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="df4df-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="df4df-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-129">Read-only</span></span><br/>  | <span data-ttu-id="df4df-130">Возвращает отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="df4df-131">**УДОСТОВЕРЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="df4df-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="df4df-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-132">Read-only</span></span><br/>  | <span data-ttu-id="df4df-133">Возвращает идентификатор, который однозначно идентифицирует пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="df4df-134">**логоннаме**</span><span class="sxs-lookup"><span data-stu-id="df4df-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="df4df-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-135">Read-only</span></span><br/>  | <span data-ttu-id="df4df-136">Возвращает имя учетной записи входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="df4df-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="df4df-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="df4df-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="df4df-138">Read/write</span></span><br/> | <span data-ttu-id="df4df-139">Задает или возвращает текущую [**квоту**](diskquotacontrol-object.md)пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="df4df-140">**куоталимиттекст**</span><span class="sxs-lookup"><span data-stu-id="df4df-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="df4df-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-141">Read-only</span></span><br/>  | <span data-ttu-id="df4df-142">Возвращает текущую [**предельную квоту**](diskquotacontrol-object.md) пользователя в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="df4df-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="df4df-143">**куотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="df4df-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="df4df-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="df4df-144">Read/write</span></span><br/> | <span data-ttu-id="df4df-145">Задает или возвращает порог предупреждения пользователя в байтах.</span><span class="sxs-lookup"><span data-stu-id="df4df-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="df4df-146">**куотасрешолдтекст**</span><span class="sxs-lookup"><span data-stu-id="df4df-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="df4df-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-147">Read-only</span></span><br/>  | <span data-ttu-id="df4df-148">Возвращает пороговое значение предупреждения пользователя в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="df4df-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="df4df-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="df4df-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="df4df-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-150">Read-only</span></span><br/>  | <span data-ttu-id="df4df-151">Возвращает текущее использование диска пользователем в байтах.</span><span class="sxs-lookup"><span data-stu-id="df4df-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="df4df-152">**куотауседтекст**</span><span class="sxs-lookup"><span data-stu-id="df4df-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="df4df-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="df4df-153">Read-only</span></span><br/>  | <span data-ttu-id="df4df-154">Возвращает текущий объем использования диска пользователем в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="df4df-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="df4df-155">Remarks</span><span class="sxs-lookup"><span data-stu-id="df4df-155">Remarks</span></span>

<span data-ttu-id="df4df-156">Каждый пользователь на томе, управляемом объектом [**дисккуотаконтрол**](diskquotacontrol-object.md) , имеет связанный с ним объект **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="df4df-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="df4df-157">Этот объект позволяет клиенту управлять параметрами отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="df4df-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="df4df-158">Существует несколько способов получить объект **дидисккуотаусер** пользователя:</span><span class="sxs-lookup"><span data-stu-id="df4df-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="df4df-159">Объекты **дидисккуотаусер** для всех пользователей с квотами на томе предоставляются в виде коллекции, и их можно перечислить.</span><span class="sxs-lookup"><span data-stu-id="df4df-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="df4df-160">Ниже приведено обсуждение того, как перечислить объекты **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="df4df-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="df4df-161">При добавлении нового пользователя метод [**adduser**](diskquotacontrol-adduser.md) возвращает объект пользователя **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="df4df-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="df4df-162">Если у вас есть имя пользователя, метод [**финдусер**](diskquotacontrol-finduser.md) возвращает объект **дидисккуотаусер** пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="df4df-163">Перечисление пользователей дисковой квоты</span><span class="sxs-lookup"><span data-stu-id="df4df-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="df4df-164">Объекты **дидисккуотаусер** для всех пользователей с квотой на том предоставляются в виде коллекции.</span><span class="sxs-lookup"><span data-stu-id="df4df-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="df4df-165">Объект [**дисккуотаконтрол**](diskquotacontrol-object.md) экспортирует стандартный метод перечислителя, позволяющий перечислить коллекцию объектов **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="df4df-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="df4df-166">Следующая процедура показывает, как выполнить перечисление с помощью Microsoft JScript (совместимой с спецификацией языка ECMA 262).</span><span class="sxs-lookup"><span data-stu-id="df4df-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="df4df-167">Аналогичную процедуру можно использовать с Visual Basic или Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="df4df-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="df4df-168">Создайте новый объект [**дисккуотаконтрол**](diskquotacontrol-object.md) .</span><span class="sxs-lookup"><span data-stu-id="df4df-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="df4df-169">Инициализируйте его с помощью [**Initialize**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="df4df-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="df4df-170">Создайте новый объект **перечислителя** JScript.</span><span class="sxs-lookup"><span data-stu-id="df4df-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="df4df-171">Используйте цикл **for** для перечисления объектов **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="df4df-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="df4df-172">Нет необходимости задавать начальное значение.</span><span class="sxs-lookup"><span data-stu-id="df4df-172">There is no need to set a starting value.</span></span> <span data-ttu-id="df4df-173">Метод **MoveNext** объекта перечислителя уведомляет метод **Item** , чтобы вернуть следующий объект **дидисккуотаусер** .</span><span class="sxs-lookup"><span data-stu-id="df4df-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="df4df-174">Метод **atEnd** возвращает **значение false** , если достигнут конец списка.</span><span class="sxs-lookup"><span data-stu-id="df4df-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="df4df-175">При необходимости используйте объект **дидисккуотаусер** , возвращенный методом **элемента** перечислителя, для получения или задания одного или нескольких свойств квоты диска связанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="df4df-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="df4df-176">В следующем фрагменте кода показано, как перечислить объекты **дидисккуотаусер** с помощью JScript.</span><span class="sxs-lookup"><span data-stu-id="df4df-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="df4df-177">Аргумент **\_ метки тома** , передаваемый функции **енумусерс** , представляет собой строковое значение, содержащее метку тома, например "C: \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="df4df-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


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



## <a name="requirements"></a><span data-ttu-id="df4df-178">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="df4df-178">Requirements</span></span>



| <span data-ttu-id="df4df-179">Требование</span><span class="sxs-lookup"><span data-stu-id="df4df-179">Requirement</span></span> | <span data-ttu-id="df4df-180">Значение</span><span class="sxs-lookup"><span data-stu-id="df4df-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df4df-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df4df-181">Minimum supported client</span></span><br/> | <span data-ttu-id="df4df-182">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df4df-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df4df-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df4df-183">Minimum supported server</span></span><br/> | <span data-ttu-id="df4df-184">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df4df-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="df4df-185">DLL</span><span class="sxs-lookup"><span data-stu-id="df4df-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df4df-186"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="df4df-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df4df-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df4df-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4df-188">**Объект оболочки**</span><span class="sxs-lookup"><span data-stu-id="df4df-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 





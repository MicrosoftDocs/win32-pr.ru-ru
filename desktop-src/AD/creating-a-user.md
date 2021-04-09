---
title: Создание пользователя
description: Чтобы создать пользователя в домен Active Directory Services, создайте объект пользователя в доменном контейнере домена, в котором нужно разместить пользователя.
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, создание пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea10d0142af650d58b61967b008b207abca2c11
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103891168"
---
# <a name="creating-a-user"></a>Создание пользователя

Чтобы создать пользователя в домен Active Directory Services, создайте объект пользователя в доменном контейнере домена, в котором нужно разместить пользователя. Пользователи могут быть созданы в корне домена, в подразделении или в контейнере.

При создании объекта пользователя необходимо также задать атрибуты, перечисленные в следующей таблице, чтобы задать объект как юридический пользователь, распознаваемый службами домен Active Directory и системой безопасности Windows.



| attribute                                       | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**cn**](/windows/desktop/ADSchema/a-cn)                         | Указывает имя объекта пользователя в каталоге. Это будет относительное различающееся имя объекта (RDN).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | Указывает строку, которая является именем, используемым для поддержки клиентов и серверов из предыдущей версии Windows. Для поддержки клиентов из предыдущей версии Windows значение [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) должно быть меньше 20 символов.<br/> Значение [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) должно быть уникальным для всех объектов субъекта безопасности в домене. Необходимо выполнить запрос к домену, чтобы проверить уникальность **SamAccountName** в домене.<br/> [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) является необязательным атрибутом. Сервер создаст случайное значение **SamAccountName** , если не указано ни одного.<br/> |



 

Можно также задать другие атрибуты. Следующие пользовательские атрибуты устанавливаются со значениями по умолчанию, если они не заданы явным образом во время создания.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a></td>
<td>Указывает, когда истечет срок действия учетной записи. Значение по умолчанию — <strong>TIMEQ_FOREVER</strong>. Это означает, что срок действия учетной записи никогда не истечет.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>нтсекуритидескриптор</strong></a></td>
<td>Дескриптор безопасности создается на основе конкретных правил. Дополнительные сведения см. <a href="how-security-descriptors-are-set-on-new-directory-objects.md">в разделе как устанавливаются дескрипторы безопасности для новых объектов каталога</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a></td>
<td>Указывает категорию пользователей. Значение по умолчанию — &quot; Person &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-name"><strong>безымян</strong></a></td>
<td>Указывает имя пользователя. По умолчанию задано значение <a href="/windows/desktop/ADSchema/a-cn"><strong>CN</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a></td>
<td>Указывает время последнего задания пароля пользователем. Значение по умолчанию равно нулю, что означает, что пользователь должен сменить пароль при следующем входе в систему.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a></td>
<td>Содержит значения, определяющие несколько функций входа и учета для пользователя.<br/> По умолчанию установлены следующие флаги:<br/>
<ul>
<li><strong>UF_ACCOUNTDISABLE</strong> - Учетная запись отключена.</li>
<li><strong>UF_PASSWD_NOTREQD</strong> - Пароль не требуется.</li>
<li><strong>UF_NORMAL_ACCOUNT</strong> - Тип учетной записи по умолчанию, представляющий обычного пользователя.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a></td>
<td>Указывает группу или группы, в которых пользователь является прямым членом. Значение по умолчанию — &quot; Пользователи домена &quot; .<br/></td>
</tr>
</tbody>
</table>



 

Пользователь создается путем привязки к нужному контейнеру, а затем используется один из следующих методов. Атрибуты [**CN**](/windows/desktop/ADSchema/a-cn) и [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) должны быть установлены до того, как пользователь зафиксируется на сервере.



| Метод                                                                       | Описание                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Иадсконтаинер. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | Атрибут [**CN**](/windows/desktop/ADSchema/a-cn) берется из параметра *бстррелативенаме* . Новый пользователь должен быть зафиксирован путем вызова метода [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) , иначе объект не будет создан. Дополнительные сведения см. в разделе [пример кода для создания пользователя](example-code-for-creating-a-user.md).<br/>                                                                                            |
| [**Идиректорйобжект:: Креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | Атрибут [**CN**](/windows/desktop/ADSchema/a-cn) берется из параметра *псзрдннаме* . Новый пользователь фиксируется при вызове [**креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) . Дополнительные сведения см. в разделе [пример кода для создания пользователя](example-code-for-creating-a-user.md).<br/>                                                                                                                |
| [Директорентриес. Add](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | Атрибут [**CN**](/windows/desktop/ADSchema/a-cn) берется из параметра *Name* . Новый объект User должен быть зафиксирован вызовом [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) , иначе объект не будет создан. Дополнительные сведения см. в разделе [Добавление объектов каталога](/previous-versions/ms180851(v=vs.90)).<br/> |



 

Новый пользователь должен быть зафиксирован на сервере, прежде чем можно будет изменить все атрибуты, кроме [**CN**](/windows/desktop/ADSchema/a-cn) и [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) . Это связано с тем, что учетная запись пользователя фактически не существует до тех пор, пока пользователь не зафиксируется. При извлечении или изменении атрибута для объекта, который не существует на сервере, возникнет ошибка. Это включает вызов метода [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) . Например, при создании пользователя с помощью [**иадсконтаинер. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)следует выполнить следующую последовательность действий.

1.  Вызовите метод [**иадсконтаинер. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) , чтобы создать пользователя в локальном кэше с указанным [**CN**](/windows/desktop/ADSchema/a-cn).
2.  Задайте для атрибута [**SamAccountName**](/windows/desktop/ADSchema/a-samaccountname) нужное значение с помощью метода [**iAds.**](/windows/desktop/api/iads/nf-iads-iads-put) Set.
3.  Теперь измените другие атрибуты, например [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol). Это ограничение также применяется к свойствам ADSI, таким как [**IADsUser. аккаунтдисаблед**](/windows/desktop/ADSI/iadsuser-property-methods), и таким методам, как [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword).
4.  Вызовите функцию [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) , чтобы зафиксировать нового пользователя на сервере.

При создании учетной записи пользователя она по умолчанию отключена. Учетную запись необходимо включить вручную или программно. Чтобы программно включить учетную запись пользователя, удалите флаг **ADS \_ УФ \_ Аккаунтдисабле** из атрибута [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

При создании учетной записи пользователя атрибут [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) для учетной записи автоматически имеет установленный флаг **УФ \_ PASSWD \_ нотрекд** , что означает, что для учетной записи пароль не требуется. Если политика безопасности домена, в которой создается учетная запись, требует пароль для всех учетных записей пользователей, необходимо удалить флаг **УФ \_ PASSWD \_ Нотрекд** из атрибута **userAccountControl** для учетной записи.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Пример кода для создания пользователя](example-code-for-creating-a-user.md)
</dt> </dl>
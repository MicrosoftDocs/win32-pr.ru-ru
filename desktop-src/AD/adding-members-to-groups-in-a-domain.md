---
title: Добавление членов в группы в домене
description: В этом разделе показано, как добавлять членов в группы в домене.
ms.assetid: be65cd4e-df3e-416b-a673-774b71ab6996
ms.tgt_platform: multiple
keywords:
- Добавление членов в группы в домене AD
- Группы AD, Добавление членов в группы в домене
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbd454348dc3eb519d03a7c5574746025c79a3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487517"
---
# <a name="adding-members-to-groups-in-a-domain"></a>Добавление членов в группы в домене

Группа может содержать любое количество пользователей, контактов или других групп в качестве членов. В следующем списке перечислены атрибуты объекта Group, управляющего членством в группе.



| attribute                                      | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**участниками**](/windows/desktop/ADSchema/a-member)<br/>     | Атрибут [**member**](/windows/desktop/ADSchema/a-member) содержит различающиеся имена объектов, являющихся членами группы.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**memberOf**](/windows/desktop/ADSchema/a-memberof)<br/> | Атрибут [**memberof**](/windows/desktop/ADSchema/a-memberof) содержит различающиеся имена групп, содержащих группу в качестве непосредственного члена. Атрибут **memberof** не содержит наследуемых данных членства в группах. Например, если Group a является членом Граупб, а Граупб является членом Граупк, то атрибут **memberof** для группы a будет содержать граупб, но не граупк.<br/> Сервер Active Directory поддерживает это свойство. Если различающееся имя добавляется к свойству [**элемента**](/windows/desktop/ADSchema/a-member) другой группы, то различающееся имя этой группы добавляется в свойство [**memberof**](/windows/desktop/ADSchema/a-memberof) этой группы.<br/> |



 

Каждый из следующих методов можно использовать для добавления члена в группу. Элемент можно добавить с помощью различающегося имени элемента или привязки к объекту-члену, а затем добавить объект члена в объект Group.

Чтобы добавить член, принадлежащий к домену нижнего уровня, в группу в домене с более ранним уровнем, используйте для различающегося имени связываемую форму строки идентификатора безопасности. Дополнительные сведения и пример кода, демонстрирующий преобразование **objectSid** в строку с возможностью привязки, см. в примере функции **Жетлдапсидбиндстрингфромвариантсид** в [примере кода для преобразования objectSid в строку с возможностью привязки](example-code-for-converting-an-objectsid-into-a-bindable-string-.md).

<dl> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IADsGroup"></span><span id="adding_members_to_a_group_by_using_iadsgroup"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IADSGROUP"></span>Добавление членов в группу с помощью Иадсграуп
</dt> <dd>

Интерфейс [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup) можно использовать для добавления членов в группу с помощью метода [**иадсграуп. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) . Привяжите к и получите интерфейс **иадсграуп** для объекта Group. Затем можно использовать метод **иадсграуп. Add** для добавления членов в группу.

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_IDirectoryObject"></span><span id="adding_members_to_a_group_by_using_idirectoryobject"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_IDIRECTORYOBJECT"></span>Добавление членов в группу с помощью Идиректорйобжект
</dt> <dd>

Интерфейс [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) можно использовать для добавления членов в группу с помощью метода [**Идиректорйобжект:: сетобжектаттрибутес**](/windows/desktop/api/iads/nf-iads-idirectoryobject-setobjectattributes) , чтобы изменить атрибут [**элемента**](/windows/desktop/ADSchema/a-member) для группы. Привяжите к и получите интерфейс **идиректорйобжект** для объекта Group. Затем используйте метод **идиректорйобжект:: сетобжектаттрибутес** , чтобы изменить атрибут **элемента** .

> [!Note]  
> Поскольку атрибут [**member**](/windows/desktop/ADSchema/a-member) имеет несколько значений, убедитесь, что для добавления различающегося имени к атрибуту **элемента** используется элемент управления **\_ \_ append attr** . Использование кода **управления \_ \_ обновлениями ADS attr** приведет к перезаписанию существующих значений **элементов** .

 

Интерфейс [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) также может использоваться для добавления членов в группу при создании группы путем указания членов в параметре *паттрибутинтриес* метода [**идиректорйобжект:: креатедсобжект**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) .

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_System.DirectoryServices"></span><span id="adding_members_to_a_group_by_using_system.directoryservices"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_SYSTEM.DIRECTORYSERVICES"></span>Добавление членов в группу с помощью System. DirectoryServices
</dt> <dd>

Пространство имен [System. DirectoryServices](/dotnet/api/system.directoryservices) можно использовать для добавления членов в группу с помощью метода **пропертивалуеколлектион. Add** в свойстве **member** объекта Group. Дополнительные сведения см. [в разделе Задание свойств объектов каталога](/previous-versions/ms180860(v=vs.90)).

</dd> <dt>

<span id="Adding_Members_to_a_Group_by_Using_the_LDAP_API"></span><span id="adding_members_to_a_group_by_using_the_ldap_api"></span><span id="ADDING_MEMBERS_TO_A_GROUP_BY_USING_THE_LDAP_API"></span>Добавление членов в группу с помощью API LDAP
</dt> <dd>

Для добавления членов в группу с помощью одной из функций [**LDAP \_ remodify \***](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s) можно использовать API [облегченного протокола доступа к каталогу](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) . Дополнительные сведения см. [в разделе Изменение записи каталога](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry).

</dd> </dl>

 


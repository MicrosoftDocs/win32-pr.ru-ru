---
description: Мбнпрофиликст \/ ... \/ Усерлогонкред (v4)
MS-HAID: WWAN\_profile\_v4.element\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 12a65d91-1917-49d4-9b58-68c60464c857
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d28c0d275b722dbba6ebc1be3363cfa3e2f6d300
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985397"
---
# <a name="span-idwwan_profile_v4element_userlogoncredspanmbnprofileextuserlogoncred-v4"></a><span id="WWAN_profile_v4.element_UserLogonCred"></span>Мбнпрофиликст \/ ... \/ Усерлогонкред (v4)

Учетные данные входа для подключения.

## <a name="element-hierarchy"></a>Иерархия элементов

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a>Синтаксис

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a>Ключ

`?`   необязательно (ноль или один)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Атрибуты и элементы

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Атрибуты

Отсутствует.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Дочерние элементы


| Дочерний элемент | Описание | 
|---------------|-------------|
| <a href="element-ignorepassword.md">игнорепассворд</a> | <p>Указывает способ обработки паролей при обновлении профилей.</p><p>Если задано значение <strong>true</strong> и профиль с тем же именем существует во время операции обновления, то пароль из этого профиля будет создан и сохранен в новом профиле.</p><p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>игнорепассворд</strong></a> v1.</p> | 
| <a href="element-password.md">Пароль</a> | <p>Указывает пароль, используемый для проверки подлинности пользователя.</p><p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-password-userlogoncred-element.md"><strong>пароля</strong></a> v1.</p> | 
| <a href="element-username.md">UserName</a> | <p>Имя пользователя, используемое для входа в систему.</p><p>Дополнительные сведения см. в документации по элементу <a href="../mbn/schema-username-userlogoncred-element.md"><strong>имени пользователя</strong></a> v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Родительские элементы


| Родительский элемент | Описание | 
|----------------|-------------|
| <a href="element-context.md">Контекст</a> | <p>Задает параметры, необходимые для установления подключения к данным.</p> | 


 

## <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p>Пространство имен</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 




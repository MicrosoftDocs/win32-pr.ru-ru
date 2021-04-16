---
description: Задает дескриптор безопасности для пространства имен, к которому подключен пользователь. Этот метод требует наличия дескриптора безопасности в двоичном формате массива байтов. При написании скрипта используйте метод Сетсекуритидескриптор.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Набор методов класса __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683600"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Набор методов \_ \_ класса системсекурити

Этот **метод задает** дескриптор безопасности для пространства имен, к которому подключен пользователь. Этот метод требует наличия дескриптора безопасности в двоичном формате массива байтов. При написании скрипта используйте метод [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class---systemsecurity.md) . Дополнительные сведения см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md).

При программировании на C++ можно управлять двоичным дескриптором безопасности с помощью [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), а также методами преобразования [**конвертсекуритидескриптортострингсекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) и [**конвертстрингсекуритидескриптортосекуритидескриптор**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Пользователь должен иметь разрешение на **запись \_ DAC** , и по умолчанию администратор имеет соответствующее разрешение. Единственной частью используемого дескриптора безопасности является неунаследованный элемент управления доступом (ACE) в списке управления доступом на уровне пользователей (DACL). Установив флаг **\_ наследования контейнера** в ACE, дескриптор безопасности влияет на дочерние пространства имен. Разрешены и запрещены ACE.

> [!Note]  
> Так как запрещено использовать ACE Deny и Allow в списке DACL, важен порядок записей ACE. Дополнительные сведения см. [в разделе Упорядочение записей ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

## <a name="syntax"></a>Синтаксис


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SD* \[ окне\]
</dt> <dd>

Массив байтов, составляющий дескриптор безопасности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение HRESULT** , указывающее состояние вызова метода. Для сценариев и Visual Basic приложений результат можно получить из [параметров out. returnValue](parsing-outparameters-objects.md). Дополнительные сведения см. в разделе [Построение объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

В следующем списке перечислены возвращаемые значения, которые являются значимыми для **набора**.

<dl> <dt>

**\_ОК**
</dt> <dd>

Метод успешно выполнен.

</dd> <dt>

**\_ \_ отказано в доступе к WBEM \_**
</dt> <dd>

Вызывающий объект не имеет достаточных прав для вызова этого метода.

</dd> <dt>

**\_метод WBEM \_ E \_ отключен**
</dt> <dd>

Попытка запуска этого метода в ОС, которая не поддерживает этот метод.

</dd> <dt>

**\_ \_ Недопустимый \_ объект для WBEM**
</dt> <dd>

SD не передает базовые тесты проверки действительности.

</dd> <dt>

**\_ \_ Недопустимый параметр "WBEM E" \_**
</dt> <dd>

SD является недопустимым по следующей причине:

-   Отсутствует список DACL.
-   Недопустимый список DACL.
-   В записи ACE установлен флаг " **\_ полная \_ запись \_ " WBEM** , а не установлен флаг **\_ \_ поставщика** **\_ частичной \_ записи \_** или WBEM.
-   ACE имеет установленный флаг **наследования \_ \_ ACE only** без флага **\_ наследования контейнера \_ ACE** .
-   В записи ACE задан неизвестный бит доступа.
-   ACE имеет установленный флаг, который отсутствует в таблице.
-   ACE имеет тип, который отсутствует в таблице.
-   Владелец и группа отсутствуют в SD.

Дополнительные сведения о флагах записи управления доступом (ACE) см. в разделе [константы безопасности WMI](wmi-security-constants.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Дополнительные сведения об изменении безопасности пространства имен программным путем или вручную см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Примеры

В следующем скрипте **показано, как использовать** setd, чтобы задать дескриптор безопасности пространства имен для корневого пространства имен и изменить его на массив байтов, показанный в *стрсд*.


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



В следующем примере кода C# используется System. Security. AccessControl. Равсекуритидескриптор для перечисления, вставки и удаления новых объектов Коммонаце в Равсекуритидескриптор. Дискретионарякл и последующего преобразования обратно в массив байтов, чтобы сохранить его посредством набора. SecurityIdentifier можно получить с помощью NTAccount и преобразования.


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_системсекурити**](--systemsecurity.md)
</dt> <dt>

[**\_\_Системсекурити:: получает**](--systemsecurity-getsd.md)
</dt> <dt>

[Константы безопасности WMI](wmi-security-constants.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Защита пространств имен WMI](securing-wmi-namespaces.md)
</dt> </dl>

 


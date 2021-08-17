---
description: Создание производного класса в WMI очень похоже на создание базового класса. Как и в случае с базовым классом, необходимо сначала определить производный класс, а затем зарегистрировать производный класс с помощью WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Создание производного класса WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cddc2b381346b2765e836bb3606cc06845280c41a7505b872098f383ac0409c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374874"
---
# <a name="creating-a-wmi-derived-class"></a>Создание производного класса WMI

Создание производного класса в WMI очень похоже на создание базового класса. Как и в случае с базовым классом, необходимо сначала определить производный класс, а затем зарегистрировать производный класс с помощью WMI. Основное отличие заключается в том, что сначала необходимо определить родительский класс, из которого требуется выполнить наследование. Дополнительные сведения см. в разделе [написание поставщика класса](writing-a-class-provider.md) и [написание поставщика экземпляра](writing-an-instance-provider.md).

Рекомендуемый способ создания классов для поставщика — MOF-файл (MOF) файлов. Несколько производных классов, связанных друг с другом, должны быть сгруппированы в MOF-файл вместе с любыми базовыми классами, из которых они наследуют свойства или методы. При помещении каждого класса в отдельный MOF-файл каждый файл должен быть скомпилирован, прежде чем поставщик сможет правильно работать.

После создания класса необходимо удалить все экземпляры класса, прежде чем можно будет выполнять следующие действия в производном классе:

-   Измените родительский класс производного класса.
-   Добавление или удаление свойств.
-   Измените типы свойств.
-   Добавление или удаление [**ключа**](key-qualifier.md) или **индексированных** квалификаторов.
-   Добавление или удаление [**одноэлементных**](standard-wmi-qualifiers.md), **динамических** или [**абстрактных**](standard-qualifiers.md) квалификаторов.

> [!Note]  
> Чтобы добавить, удалить или изменить свойство или квалификатор, вызовите [**IWbemServices::P уткласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) или [**\_ SWbemObject.**](swbemobject-put-.md) Set и установите для параметра flag значение "Force Mode". [**Абстрактный**](standard-qualifiers.md) квалификатор можно использовать только в том случае, если родительский класс является абстрактным.

 

При объявлении производного класса Обратите внимание на следующие правила и ограничения.

-   Родительский класс производного класса должен уже существовать.

    Объявление родительского класса может находиться в том же MOF-файле, что и производный класс, или в другом файле. Если родительский класс неизвестен, компилятор создает ошибку времени выполнения.

-   Производный класс может иметь только один родительский класс.

    Инструментарий WMI не поддерживает множественное наследование. Однако у родительского класса может быть множество производных классов.

-   Можно определить индексы для производных классов, но WMI не использует эти индексы.

    Поэтому указание индекса в производном классе не повышает производительность запросов экземпляров производного класса. Можно повысить производительность запроса в производном классе, указав индексированные свойства для родительского класса производного класса.

-   Определения производных классов могут быть более сложными и могут включать такие функции, как псевдонимы, квалификаторы и разновидности квалификаторов.

    Дополнительные сведения см. в разделе [Создание псевдонима](creating-an-alias.md) и [Добавление квалификатора](adding-a-qualifier.md).

-   Если вы хотите изменить квалификатор, измените значение свойства базового класса по умолчанию или более строго введите ссылку или внедренное свойство объекта базового класса, необходимо снова объявить весь базовый класс.
-   Максимальное число свойств, которое можно определить в классе WMI, — 1024.

> [!Note]  
> Классы не могут быть изменены во время выполнения поставщиков. необходимо прерывать действие, изменить класс, а затем перезапустить службу управления Windows. Обнаружение изменения класса в настоящее время невозможно.

 

Как и в случае с базовым классом, наиболее распространенным применением этого метода будет клиентские приложения. Однако поставщик может также создать производный класс. Дополнительные сведения см. в разделе [Создание базового класса](creating-a-base-class.md) и [запись поставщика класса](writing-a-class-provider.md).

В примере кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.


```C++
#include <wbemidl.h>
```



В следующей процедуре описывается создание производного класса с помощью C++.

**Создание производного класса с помощью C++**

1.  Нахождение базового класса с вызовом [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    В следующем примере кода показано, как можно разместить пример базового класса.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Создайте производный объект из базового класса с помощью вызова [**ивбемклассобжект:: спавндериведкласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).

    В следующем примере кода показано, как создать объект производного класса.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Задайте имя для класса, задав системное свойство **\_ \_ класса** с помощью вызова метода [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    В следующем примере кода показано, как присвоить имя производному классу.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  Создайте дополнительные свойства с помощью [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    В следующем примере кода показано, как создать дополнительные свойства.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Сохраните новый класс, вызвав [**IWbemServices::P уткласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    В следующем примере кода показано, как сохранить новый производный класс.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

Следующий пример кода сочетает примеры кода, описанные в предыдущей процедуре, чтобы описать, как создать производный класс с помощью API WMI.


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



В следующей процедуре описывается определение производного класса с помощью MOF-кода.

**Определение производного класса с помощью MOF-кода**

1.  Определите производный класс с помощью ключевого слова **Class** , укажите имя производного класса и имя родительского класса, разделенное двоеточием.

    В следующем примере кода описывается реализация производного класса.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  По завершении Скомпилируйте MOF-код с помощью компилятора MOF.

    Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание класса](creating-a-class.md)
</dt> </dl>

 

 




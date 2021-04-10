---
description: Рекомендуемый способ создания нового базового класса WMI для поставщика WMI — файл MOF-файл (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Создание базового класса WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999377"
---
# <a name="creating-a-wmi-base-class"></a>Создание базового класса WMI

Рекомендуемый способ создания нового базового класса WMI для поставщика WMI — файл MOF-файл (MOF). Можно также создать базовый класс с помощью [API COM для WMI](com-api-for-wmi.md). Несмотря на то, что в скрипте можно создать базовый или производный класс, без поставщика, предоставляющего данные классу и его подклассам, класс не полезен.

В этом разделе обсуждаются следующие разделы:

-   [Создание базового класса с помощью MOF](#creating-a-base-class-using-mof)
-   [Создание базового класса с помощью C++](#creating-a-base-class-with-c)
-   [См. также](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>Создание базового класса с помощью MOF

Классы WMI обычно полагаются на наследование. Перед созданием базового класса проверьте классы модель CIM (CIM), доступные в распределенном управлении Task Force ([DMTF](https://www.dmtf.org/)).

Если многие производные классы будут использовать одни и те же свойства, помещайте эти свойства и методы в базовый класс. Максимальное число свойств, которое можно определить в классе WMI, — 1024.

При создании базового класса Обратите внимание на приведенный ниже список правил для имен классов.

-   Используйте как прописные, так и строчные буквы.
-   Имя класса должно начинаться с буквы.
-   Не используйте символ подчеркивания в начале или в конце.
-   Определите все остальные символы как буквы, цифры или символы подчеркивания.
-   Используйте единообразное соглашение об именовании.

    В отличие от этого, хорошее соглашение об именовании для класса — это два компонента, Соединенные подчеркиванием. По возможности имя поставщика должно состоять из первой половины имени, а описательное имя класса должно быть второй частью.

> [!Note]  
> Классы не могут быть изменены во время выполнения поставщиков. Необходимо прерывать действие, изменить класс, а затем перезапустить службу управления Windows. Обнаружение изменения класса в настоящее время невозможно.

 

В MOF Создайте базовый класс, присвоив ему ключевое слово **Class** , но не указывая родительский класс.

**Создание базового класса с помощью MOF-кода**

1.  Используйте ключевое слово **Class** с именем нового класса, за которым следует пара фигурных скобок и точка с запятой. Добавьте свойства и методы класса между фигурными скобками. Ниже приведен пример кода.

    В следующем примере кода показано, как должен быть определен базовый класс.

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    В следующем примере кода показано неправильное определение базового класса.

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  Добавьте [*Квалификаторы*](gloss-q.md) любого класса перед ключевым словом class, чтобы изменить способ использования класса. Поместите квалификаторы между квадратными скобками. Дополнительные сведения об квалификаторах для изменения классов см. в разделе [квалификаторы WMI](wmi-qualifiers.md). Используйте **абстрактный** квалификатор, чтобы указать, что нельзя создать экземпляр этого класса напрямую. Абстрактные классы часто используются для определения свойств или методов, которые будут использоваться несколькими производными классами. Дополнительные сведения см. [в разделе Создание производного класса](creating-a-derived-class.md).

    В следующем примере кода класс определяется как абстрактный и определяет поставщик, который будет предоставлять данные. [*Разновидность*](gloss-f.md) квалификатора **ToSubClass** указывает, что сведения в квалификаторе **поставщика** наследуются производными классами.

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  Добавьте свойства и методы класса в квадратные скобки перед именем свойства или метода. Дополнительные сведения см. в разделе [Добавление свойства](adding-a-property.md) и [Создание метода](creating-a-method.md). Эти свойства и методы можно изменить с помощью квалификаторов MOF. Дополнительные сведения см. [в разделе Добавление квалификатора](adding-a-qualifier.md).

    В следующем примере кода показано, как изменить свойства и методы с квалификаторами MOF.

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  Сохраните MOF-файл с расширением. mof.
5.  Зарегистрируйте класс в WMI, запустив [**Mofcomp.exe**](mofcomp.md) для файла.

    **mofcomp.exe** *невмоф. mof*

    Если не использовать параметр **-N** или \# [**пространство имен директивы pragma**](pragma-namespace.md) для указания пространства имен, скомпилированные классы MOF будут храниться в корневом \\ пространстве имен по умолчанию в репозитории. Дополнительные сведения см. в разделе [**mofcomp**](mofcomp.md).

В следующем примере кода объединены примеры MOF-кода, обсуждаемые в предыдущей процедуре, и показано, как создать базовый класс в корневом \\ пространстве имен CIMV2 с помощью MOF.

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

Дополнительные сведения см. в разделе [Создание производного класса](creating-a-derived-class.md) для примера динамического класса, производного от этого базового класса.

## <a name="creating-a-base-class-with-c"></a>Создание базового класса с помощью C++

Создание базового класса с помощью API инструментария WMI является главным набором команд размещения, определяющих класс и регистрирующих класс с помощью WMI. Основное назначение этого API заключается в том, чтобы позволить клиентским приложениям создавать базовые классы. Однако поставщик также может использовать этот API для создания базового класса. Например, если вы считаете, что MOF-код поставщика не будет установлен должным образом, вы можете указать поставщику автоматически создавать правильные классы в репозитории WMI. Дополнительные сведения о поставщиках см. [в разделе Написание поставщика класса](writing-a-class-provider.md).

> [!Note]  
> Классы не могут быть изменены во время выполнения поставщиков. Необходимо прерывать действие, изменить класс, а затем перезапустить службу управления Windows. Обнаружение изменения класса в настоящее время невозможно.

 

Для правильной компиляции кода требуется следующая ссылка.


```C++
#include <wbemidl.h>
```



Новый базовый класс можно создать программно с помощью [API COM для WMI](com-api-for-wmi.md).

**Создание нового базового класса с помощью API инструментария WMI**

1.  Получите определение для нового класса, вызвав метод [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) с параметром *стробжектпас* , для которого задано значение **null** .

    В следующем примере кода показано, как получить определение для нового класса.

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  Задайте имя для класса, задав системное свойство **\_ \_ класса** с помощью вызова метода [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    В следующем примере кода показано, как присвоить имя классу, задав системное свойство **\_ \_ класса** .

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  Создайте ключевое свойство или свойства, вызвав [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    В следующем примере кода показано, как создать свойство [**index**](swbemrefreshableitem-index.md) , помеченное как ключевое свойство на шаге 4.

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  Присоедините квалификатор [**Key**](standard-qualifiers.md) Standard к свойству ключа, вызвав метод [**Ивбемклассобжект:: жетпропертикуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) , а затем метод [**ивбемкуалифиерсет::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    В следующем примере кода показано, как присоединить квалификатор [**Key**](standard-qualifiers.md) Standard к свойству ключа.

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  Создайте другие свойства класса с помощью [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    В следующем примере кода показано, как создать дополнительные свойства.

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  Зарегистрируйте новый класс, вызвав [**IWbemServices::P уткласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Так как вы не можете определить ключи и индексы после регистрации нового класса, убедитесь, что все свойства определены до вызова [**путкласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    В следующем примере кода показано, как зарегистрировать новый класс.

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

В следующем примере кода объединены примеры кода, описанные в предыдущей процедуре, и показано, как создать базовый класс с помощью API WMI.


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание класса](creating-a-class.md)
</dt> </dl>

 

 




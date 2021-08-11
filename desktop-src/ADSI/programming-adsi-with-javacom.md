---
title: Программирование ADSI с помощью Java/COM
description: Используя виртуальную машину Майкрософт для Java (Microsoft VM) и Microsoft Java Compiler, вы можете получить доступ ко всем функциям ADSI, предоставляемым через любые COM-компоненты ADSI, из приложения Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Программирование ADSI с помощью Java/COM AD
- ADSI ADSI, использование, программирование Java/COM для
- ADSI ADSI, пример кода Java
- ADSI ADSI, пример кода Java, привязка к объекту ADSI и вызов методов для этого объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4778d1d1f71920f880fe38a71874283f7cd8628ae0376b3f9ce227305ab184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178978"
---
# <a name="programming-adsi-with-javacom"></a>Программирование ADSI с помощью Java/COM

Используя виртуальную машину Майкрософт для Java (Microsoft VM) и Microsoft Java Compiler, вы можете получить доступ ко всем функциям ADSI, предоставляемым через любые COM-компоненты ADSI, из приложения Java/COM. В следующем примере кода Java показаны элементы, необходимые для привязки к объекту ADSI и вызова методов для этого объекта. Необходимые функции API ADSI и методы объектов предоставляются через Activeds.dll.


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



Аргумент в первом операторе **Import** ссылается на классы-оболочки Java, упакованные в Activeds.dll. Используйте Visual J++ для создания классов-оболочек и включения их в проект, следуя приведенной ниже процедуре.

**Создание классов-оболочек и их включение в проект**

1.  в проекте Visual J++ выберите **добавить оболочку Com...** в меню **Project** .
2.  Выберите "Библиотека типов Active Directory" в списке **установленные компоненты:** в диалоговом окне оболочки COM. Если библиотека типов не отображается в списке, нажмите кнопку **Обзор...** , перейдите в каталог, где хранится активедс. tlb, а затем выберите библиотеку типов.

Visual J++ создает пакет активедс для классов-оболочек Java и включает пакет в путь по умолчанию для проекта. дополнительные сведения см. в разделе пакет активедс на панели **Project "обзор** " в окне Visual J++.

Чтобы получить объект ADSI, который не может быть создан одновременно, используйте одну из предоставляемых функций API интерфейса ADSI, например [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) или [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), которые также упаковываются в Activeds.dll. Microsoft J/Direct предоставляет доступ к этим и другим собственным API. Это продемонстрировано в двух последних строках примера кода выше.

При компиляции убедитесь, что расширение языка Майкрософт включено. для этого выберите пункт **<project> свойства...** в меню **Project** в окне проекта Visual J++. Затем откройте вкладку **Компиляция** в диалоговом окне **<project> Свойства** . Снимите флажок **Отключить расширения языка Майкрософт** . При компиляции из командной строки используйте параметр "/КС-", например:

**JVC/КС-Симплеадси. Java**

Наконец, чтобы виртуальная машина загрузила COM-компонент, в системном пути должна быть видна библиотека динамической компоновки (DLL). Если возвращается ошибка "Java. lang. Унсатисфиедлинкеррор", установите путь, чтобы включить путь, содержащий требуемую библиотеку DLL. Например, если Activeds.dll установлен в c: \\ ADSI \\ lib, выполните в командной строке следующую команду:

**задать путь =% PATH%; в. \\ \\ Библиотека ADSI**

 

 





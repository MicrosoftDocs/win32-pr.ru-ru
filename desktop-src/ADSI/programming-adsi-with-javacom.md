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
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887503"
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

1.  В проекте Visual J++ выберите **добавить оболочку COM...** в меню **проект** .
2.  Выберите "Библиотека типов Active Directory" в списке **установленные компоненты:** в диалоговом окне оболочки COM. Если библиотека типов не отображается в списке, нажмите кнопку **Обзор...** , перейдите в каталог, где хранится активедс. tlb, а затем выберите библиотеку типов.

Visual J++ создает пакет активедс для классов-оболочек Java и включает пакет в путь по умолчанию для проекта. Дополнительные сведения см. в разделе пакет активедс в области **просмотра проекта** в окне Visual J++.

Чтобы получить объект ADSI, который не может быть создан одновременно, используйте одну из предоставляемых функций API интерфейса ADSI, например [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) или [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), которые также упаковываются в Activeds.dll. Microsoft J/Direct предоставляет доступ к этим и другим собственным API. Это продемонстрировано в двух последних строках примера кода выше.

При компиляции убедитесь, что расширение языка Майкрософт включено. Для этого выберите пункт **<project> Свойства...** в меню **проект** в окне проекта Visual J++. Затем откройте вкладку **Компиляция** в диалоговом окне **<project> Свойства** . Снимите флажок **Отключить расширения языка Майкрософт** . При компиляции из командной строки используйте параметр "/КС-", например:

**JVC/КС-Симплеадси. Java**

Наконец, чтобы виртуальная машина загрузила COM-компонент, в системном пути должна быть видна библиотека динамической компоновки (DLL). Если возвращается ошибка "Java. lang. Унсатисфиедлинкеррор", установите путь, чтобы включить путь, содержащий требуемую библиотеку DLL. Например, если Activeds.dll установлен в c: \\ ADSI \\ lib, выполните в командной строке следующую команду:

**задать путь =% PATH%; в. \\ \\ Библиотека ADSI**

 

 





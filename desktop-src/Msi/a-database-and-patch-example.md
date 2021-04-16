---
description: Приложение может использовать функцию Мсиопендатабасе для открытия новой или существующей базы данных установки (MSI-файла) или пакета исправлений (MSP-файл). Приложение проверяет возвращаемое значение Мсиопендатабасе перед использованием маркера базы данных.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Пример базы данных и исправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662981"
---
# <a name="a-database-and-patch-example"></a>Пример базы данных и исправления

Приложение может использовать функцию [**мсиопендатабасе**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) для открытия новой или существующей базы данных установки (MSI-файла) или пакета исправлений (MSP-файл). Приложение проверяет возвращаемое значение **мсиопендатабасе** перед использованием маркера базы данных.

В следующих примерах используются переменные типа **пмсихандле** , определенные в MSI. h. Рекомендуется использовать тип **пмсихандле** , так как установщик закрывает объекты **пмсихандле** , когда они выходят за пределы области действия, тогда как приложение должно закрыть объекты **мсихандле** , вызвав [**мсиклосехандле**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). Дополнительные сведения см. в разделе [Использование пмсихандле вместо Handle](windows-installer-best-practices.md) в [рекомендациях по установщик Windows](windows-installer-best-practices.md).

В следующем примере открывается база данных, sample.msi, только для чтения. [**Мсиопендатабасе**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) выполняется, только если sample.msi существует в каталоге c: \\ Test. После успешного выполнения возвращенный обработчик базы данных можно использовать для запроса данных в пакете установки с помощью [**мсидатабасеопенвиев**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) и [**мсижетсуммаринформатион**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



В следующем примере открывается база данных для чтения и записи. Если приложение вызывает [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), сохраняются все изменения, внесенные в базу данных. Если приложение не вызывает **мсидатабасекоммит**, в базу данных не вносятся изменения.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



В следующем примере берется существующая база данных, text.msi и создается новая база данных newtest.msi. Любые внесенные изменения можно сохранить в новой базе данных, вызвав [**мсидатабасекоммит**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Существующая база данных, указанная в параметре *сздатабасепас* , не изменена.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



В следующем примере открывается пакет исправлений установщик Windows (MSP-файл) только для чтения. Возвращенный маркер исправления можно использовать для определения ящиков и преобразования подхранилищ, включенных в пакет исправлений, с помощью запросов к таблицам [ \_ Streams](-streams-table.md) и [ \_ Storage](-storages-table.md) .

**Установщик Windows 2,0:** Не поддерживается. Начиная с установщик Windows 3,0, приложение может запрашивать [таблицу мсипатчсекуенце](msipatchsequence-table.md) , присутствующую в пакете исправлений, который использует новые сведения о последовательности исправлений.


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 




---
description: В этом разделе описывается реализация компонента в виде библиотеки динамической компоновки (DLL) в Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Функции DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105650417"
---
# <a name="dll-functions"></a>Функции DLL

В этом разделе описывается реализация компонента в виде библиотеки динамической компоновки (DLL) в Microsoft DirectShow.

Библиотека DLL должна реализовывать следующие функции, чтобы ее можно было зарегистрировать, отменить регистрацию и загрузить в память.

-   [*DllMain*](/windows/desktop/Dlls/dllmain): точка входа библиотеки DLL. Имя *DllMain* — это заполнитель для имени определяемой библиотекой функции. В реализации DirectShow используется имя **дллентрипоинт**. Дополнительные сведения см. в разделе пакет SDK для платформы.
-   [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): создает экземпляр фабрики класса. Описано в предыдущих разделах.
-   [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): запрашивает возможность безопасной выгрузки библиотеки DLL.
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): создает записи реестра для библиотеки DLL.
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): удаляет записи реестра для библиотеки DLL.

Из них первые три реализуются с помощью DirectShow. Если шаблон фабрики предоставляет функцию инициализации в переменной-члене [**m \_ лпфнинит**](cfactorytemplate-m-lpfninit.md) , эта функция вызывается из функции точки входа библиотеки DLL. Дополнительные сведения о том, когда система вызывает функцию точки входа библиотеки DLL, см. в разделе [*DllMain*](/windows/desktop/Dlls/dllmain).

Необходимо реализовать [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), но DirectShow предоставляет функцию с именем [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) , которая выполняет необходимую работу. Компонент может просто обернуть эту функцию, как показано в следующем примере:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



Однако в [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) можно настроить процесс регистрации по мере необходимости. Если ваша библиотека DLL содержит фильтр, может потребоваться дополнительная работа. Дополнительные сведения см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md).

В файле определения модуля (DEF) Экспортируйте все функции DLL, кроме функции точки входа. Ниже приведен пример DEF-файла.


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



Библиотеку DLL можно зарегистрировать с помощью служебной программы Regsvr32.exe.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 

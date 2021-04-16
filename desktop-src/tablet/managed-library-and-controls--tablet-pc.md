---
description: Чтобы создать приложения для планшетных ПК на C \# и Visual Basic .NET, проект в Microsoft Visual Studio .NET должен содержать ссылку на сборки управляемой библиотеки для планшетных ПК. Это обеспечивает доступ к управляемой модели объектов и элементам управления.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Управляемая библиотека и элементы управления (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712622"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Управляемая библиотека и элементы управления (планшетный ПК)

Чтобы создать приложения для планшетных ПК на C \# и Visual Basic .NET, проект в Microsoft Visual Studio .NET должен содержать ссылку на сборки управляемой библиотеки для планшетных ПК. Это обеспечивает доступ к управляемой модели объектов и элементам управления.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# и visual Basic.NET

В Windows Vista сборки управляемой библиотеки Tablet PC устанавливаются по умолчанию в двух каталогах:

-   <systemdrive>: \\ Program Files \\ Common Files \\ Microsoft Shared \\ Ink Directory
-   <systemdrive>: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin

Чтобы добавить ссылку на управляемые библиотеки платформы Tablet PC в Microsoft Visual Studio .NET:

1.  Откройте проект Visual Studio .NET.
2.  В меню **Проект** выберите пункт **Добавить ссылку**.
3.  На вкладке **.NET** в диалоговом окне **Добавление ссылки** в списке компоненты выберите **Microsoft Tablet PC API**.
4.  Нажмите кнопку **выбрать**, а затем кнопку **ОК**.

Чтобы добавить ссылку на API анализа рукописного ввода в Visual Studio .NET, выполните следующие действия.

1.  Откройте проект Microsoft Visual Studio .NET.
2.  В меню **Проект** выберите пункт **Добавить ссылку**.
3.  На вкладке **.NET** в диалоговом окне **Добавление ссылки** в списке компоненты выберите пункт **управляемая библиотека анализа рукописного ввода Microsoft Tablet PC**.
4.  Нажмите кнопку **выбрать**, а затем кнопку **ОК**.

> [!Note]  
> При компиляции приложений, использующих Microsoft. Ink в Visual Studio 2005, необходимо выбрать **проект**, выбрать **свойства**, выбрать **сборку** и задать целевую платформу = x86. Этот параметр недоступен в продуктах Microsoft Visual Studio Express.

 

 

 




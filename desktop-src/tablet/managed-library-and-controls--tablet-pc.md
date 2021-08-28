---
description: чтобы создать приложения для планшетных пк на C \# и Visual Basic .net, проект в Microsoft Visual Studio .net должен содержать ссылку на сборки управляемой библиотеки для планшетных пк. Это обеспечивает доступ к управляемой модели объектов и элементам управления.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Управляемая библиотека и элементы управления (планшетный ПК)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b4096ba54d3cd882b3ee50469d94792b4a46ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884281"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Управляемая библиотека и элементы управления (планшетный ПК)

чтобы создать приложения для планшетных пк на C \# и Visual Basic .net, проект в Microsoft Visual Studio .net должен содержать ссылку на сборки управляемой библиотеки для планшетных пк. Это обеспечивает доступ к управляемой модели объектов и элементам управления.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# и Visual Basic .net

в Windows Vista сборки управляемой библиотеки Tablet PC устанавливаются по умолчанию в двух каталогах:

-   &lt;systemdrive &gt; : \\ Program Files \\ Common Files \\ Microsoft Shared \\ Ink Directory
-   &lt;systemdrive &gt; : \\ Program files \\ Microsoft sdks \\ Windows \\ v 6.0 \\ Bin

чтобы добавить ссылку на управляемые библиотеки платформы Tablet PC в Microsoft Visual Studio .net:

1.  откройте проект Visual Studio .net.
2.  В меню **Проект** щелкните команду **Добавить ссылку**.
3.  На вкладке **.NET** в диалоговом окне **Добавление ссылки** в списке компоненты выберите **Microsoft Tablet PC API**.
4.  Нажмите кнопку **выбрать**, а затем кнопку **ОК**.

чтобы добавить ссылку на api анализа рукописного ввода в Visual Studio .net:

1.  откройте проект Microsoft Visual Studio .net.
2.  В меню **Проект** щелкните команду **Добавить ссылку**.
3.  На вкладке **.NET** в диалоговом окне **Добавление ссылки** в списке компоненты выберите пункт **управляемая библиотека анализа рукописного ввода Microsoft Tablet PC**.
4.  Нажмите кнопку **выбрать**, а затем кнопку **ОК**.

> [!Note]  
> при компиляции приложений, использующих Microsoft. Ink на Visual Studio 2005, необходимо выбрать **Project**, выбрать **свойства**, выбрать **сборку** и задать целевую платформу = x86. этот параметр недоступен в продуктах Microsoft Visual Studio Express.

 

 

 




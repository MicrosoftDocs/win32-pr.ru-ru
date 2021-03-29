---
title: Установка метода EAP
description: Следуйте приведенным ниже инструкциям, чтобы установить реализованный пользователем метод EAP на клиентском компьютере с EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93e7796c216b5f60b7a46768ed9db9ca913482d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790866"
---
# <a name="installing-an-eap-method"></a>Установка метода EAP

Следуйте приведенным ниже инструкциям, чтобы установить реализованный пользователем метод EAP на клиентском компьютере с EAPHost.

-   Реализуйте [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) и [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) для библиотеки DLL метода EAP. Эти функции добавляют и удаляют соответствующие разделы реестра для метода EAP во время установки и (удаления) процесса.

    Сведения о конкретных разделах реестра, связанных с установкой метода EAP, см. в разделе [Настройка реестра для методов EAP](registry-keys-for-eap-methods.md) .

-   Установите библиотеку DLL, содержащую реализацию метода EAP, с помощью следующей команды консоли.

     *&lt; Имя &gt;regsvr32.exeDLL*

    Чтобы удалить библиотеку DLL, используйте следующую команду консоли:

    **regsvr32.exe** **/u** *&lt; имя &gt; библиотеки*

-   Перезапустите службу EAPHost.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование EAPHost](using-eap-host.md)
</dt> </dl>

 

 
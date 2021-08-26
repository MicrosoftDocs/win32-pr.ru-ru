---
title: Установка метода EAP
description: Следуйте приведенным ниже инструкциям, чтобы установить реализованный пользователем метод EAP на клиентском компьютере с EAPHost.
ms.assetid: c353550f-73a7-4195-81ea-544f74abc880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e047c5a8f0bc4cedcc207016d6f66530b392869839dda128635cd31ac459011a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021584"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование EAPHost](using-eap-host.md)
</dt> </dl>

 

 
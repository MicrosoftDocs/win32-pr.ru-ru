---
title: Вызов интерфейсов API Active Accessibility
description: Microsoft Active Accessibility предоставляет прикладные программные интерфейсы (API) как для клиентов, так и для серверов.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a239495fddbcaf2275f095abc889295568b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070147"
---
# <a name="calling-active-accessibility-apis"></a>Вызов интерфейсов API Active Accessibility

Microsoft Active Accessibility предоставляет прикладные программные интерфейсы (API) как для клиентов, так и для серверов. Большинство из них реализованы в библиотеке динамической компоновки Microsoft Active Accessibility, Oleacc.dll, но [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)и [**унхуквиневент**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) реализуются в user32.dll, который является основным компонентом операционной системы Microsoft Windows.

На компьютерах под управлением Windows 95 или Microsoft Windows NT 4,0 не установлены Oleacc.dll и установлена правильная версия user32.dll, так как Microsoft Active Accessibility был включен в составе последующих версий Windows. В результате приложения, работающие на этих платформах, явным образом связываются с Oleacc.dll во время выполнения с помощью функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) , а не с использованием библиотек импорта. Active Accessibility 1,3 поддерживает Windows 95 и Microsoft Windows NT 4,0. Более ранние версии Windows не поддерживаются корпорацией Майкрософт Active Accessibility.

Серверные приложения используют функцию [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения адреса функции Microsoft Active Accessibility, а затем выполняют вызов через указатель функции. При вызове функции, реализованной в Oleacc.dll, серверные приложения используют в вызове **GetProcAddress** маркер, возвращенный из [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) . При вызове функции, определенной в user32.dll, серверные приложения вызывают [**Ошибка GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) , УКАЗАВ "user32", и используйте возвращенный маркер модуля в вызове **GetProcAddress**.

Например, если приложение использует [**нотифивиневент**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), оно вызывает [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) с помощью обработчика модуля user32.dll, чтобы получить адрес функции. Если вызов прошел успешно (это означает, что эта версия Windows поддерживает Microsoft Active Accessibility), то в приложении устанавливается флаг, указывающий, что вызов **нотифивиневент** может быть защищен. Адрес, полученный из **GetProcAddress** , хранится в переменной указателя функции и используется во всем коде.

 

 
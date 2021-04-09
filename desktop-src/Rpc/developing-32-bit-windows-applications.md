---
title: Разработка приложений для Windows RPC
description: При установке пакета средств разработки программного обеспечения для платформы (SDK) автоматически устанавливаются следующие среды разработки RPC, библиотеки времени выполнения и средства.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070511"
---
# <a name="developing-rpc-windows-applications"></a>Разработка приложений для Windows RPC

При установке пакета средств разработки программного обеспечения для платформы (SDK) автоматически устанавливаются следующие среды разработки RPC, библиотеки времени выполнения и средства.

-   Заголовок языка C/C++ (. H) файлы
-   Файлы библиотек импорта RPC (lib)
-   Примеры программ
-   Справочные файлы по RPC
-   Служебная программа **uuidgen**

При установке Windows устанавливаются следующие компоненты:

-   Библиотеки DLL времени выполнения RPC
-   Локатор Майкрософт (не поддерживается в Windows Vista и более поздних версиях)
-   Конечная точка RPC — службы сопоставления

Следующие библиотеки импорта RPC.



| Импорт библиотеки | Описание                |
|----------------|----------------------------|
| Rpcns4. lib     | Функции Name-Service     |
| Rpcrt4. lib     | Функции времени выполнения Windows |



 

> [!Note]  
> Rpcns4. lib устарела и больше не поддерживается.

 

Для поддержки нижнего уровня включены следующие библиотеки RPC.



| Библиотека динамической компоновки | Описание:                 | Платформа                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Транспорт клиента именованного канала | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Транспорт серверных именованных каналов | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | Клиентский транспорт TCP/IP     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Транспорт TCP/IP сервера     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Клиентский транспорт NetBIOS    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Транспорт NetBIOS сервера    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Транспорт клиента SPX        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Транспорт сервера SPX        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Клиентский транспорт IPX        | Windows NT                         |
| Rpcdgs6.dll          | Транспорт сервера IPX        | Windows NT                         |
| Rpcdgc3.dll          | Клиентский транспорт UDP        | Windows NT                         |
| Rpcdgs3.dll          | Транспорт UDP сервера        | Windows NT                         |



 

Также потребуется компилятор язык MIDL (MIDL). Дополнительные сведения см. [в разделе Использование КОМПИЛЯТОРА MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 
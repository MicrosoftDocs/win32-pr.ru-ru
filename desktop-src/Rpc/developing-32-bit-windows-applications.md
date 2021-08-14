---
title: разработка приложений Windows RPC
description: При установке пакета средств разработки программного обеспечения для платформы (SDK) автоматически устанавливаются следующие среды разработки RPC, библиотеки времени выполнения и средства.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ddb48a38faadb8235064fa735fa8a75a80a62308990373ab1971d4a6cd9ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930799"
---
# <a name="developing-rpc-windows-applications"></a>разработка приложений Windows RPC

При установке пакета средств разработки программного обеспечения для платформы (SDK) автоматически устанавливаются следующие среды разработки RPC, библиотеки времени выполнения и средства.

-   Заголовок языка C/C++ (. H) файлы
-   Файлы библиотек импорта RPC (lib)
-   Примеры программ
-   Справочные файлы по RPC
-   Служебная программа **uuidgen**

при установке Windows устанавливаются следующие компоненты:

-   Библиотеки DLL времени выполнения RPC
-   локатор майкрософт (не поддерживается в Windows Vista и более поздних версиях)
-   Конечная точка RPC — службы сопоставления

Следующие библиотеки импорта RPC.



| Импорт библиотеки | Описание                |
|----------------|----------------------------|
| Rpcns4. lib     | Функции Name-Service     |
| Rpcrt4. lib     | Windows функции времени выполнения |



 

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

 

 
---
title: Реклама в интерфейсах сервера
description: Серверная часть приложения, использующего автоматические дескрипторы, должна вызывать функцию Рпкнсбиндинжекспорт, чтобы сделать сведения о привязке сервера доступными для клиентов.
ms.assetid: d15fd8da-3afd-4031-95d1-b76a0ad9a20d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45955ac7228018d8ddebbc7c156031648091b6f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068021"
---
# <a name="advertising-server-interfaces"></a>Реклама в интерфейсах сервера

Серверная часть приложения, использующего автоматические дескрипторы, должна вызывать функцию [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) , чтобы сделать сведения о привязке сервера доступными для клиентов. Для автоматической обработки дескрипторов привязки на сервере, доступном для клиента, должна выполняться служба имен. Реализация службы имен (Майкрософт), локатор Майкрософт, управление автоматическими дескрипторами. Серверные приложения, использующие неявные и явные дескрипторы привязки, также могут объявлять свое присутствие в базе данных службы имен.

Как правило, сервер вызывает следующие функции времени выполнения:

``` syntax
/* auto handle server application (fragment) */
 
//interface header file that the MIDL compiler generates
#include "auto.h" 
 
void main(void)
{
    RpcUseProtseqEp(...);
    RpcServerRegisterIf(...);
    RpcServerInqBindings(...);
    RpcNsBindingExport(...);
    ...
}
```

Вызовы первых двух функций в этом фрагменте кода похожи на [пример Hello, World](tutorial.md). Эти функции позволяют клиенту получить сведения о привязке. Вызовы [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) и [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) помещают сведения в базу данных службы имен. Вызов [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) заполняет вектор привязки допустимыми дескрипторами привязки перед экспортом дескрипторов в службу имен. После того как программа сервера экспортирует дескрипторы в базу данных, клиент (или клиентские заглушки) может вызвать [**рпкнсбиндингимпортбегин**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) и [**рпкнсбиндингимпортнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) для получения этих сведений. Дополнительные сведения см. в разделе [Поиск хостовых систем сервера](finding-server-host-systems.md).

Вызовы [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) и [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) и связанных с ними структур данных выглядят следующим образом:

``` syntax
RPC_BINDING_VECTOR * pBindingVector;
RPCSTATUS status;
 
status = RpcServerInqBindings(&pBindingVector);
 
status = RpcNsBindingExport(
                fNameSyntaxType,      // name syntax type 
                pszAutoEntryName,     // nsi entry name 
                autoh_ServerIfHandle, // if server handle
                pBindingVector,       // set in previous call 
                NULL);                // UUID vector
```

Обратите внимание, что параметр [**Рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings) *пбиндингвектор* является указателем на указатель [**на \_ \_ вектор привязки RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_binding_vector). Также помните, что после каждого вызова [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta) должен следовать вызов [**рпкбиндингвекторфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree).

Чтобы удалить экспортированный интерфейс из базы данных службы имен, сервер вызывает [**рпкнсбиндингунекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) , как показано ниже.

``` syntax
status = RpcNsBindingUnexport(
                fNameSyntaxType, 
                pszAutoEntryName,  
                auto_ServerIfHandle,
                NULL);              // unexport handles only
```

Функция [**рпкнсбиндингунекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexporta) должна использоваться только при окончательном удалении службы. Его не следует использовать при временном отключении службы, например при выключении сервера для обслуживания. Серверная программа может зарегистрироваться в базе данных службы имен, но она будет недоступна, так как сервер временно отключен от сети. Клиентское приложение должно содержать код обработки исключений для такого условия.

Дополнительные сведения о содержимом и формате базы данных службы имен см. в разделе [база данных службы имен RPC](the-rpc-name-service-database.md).

Приложения могут использовать службу Active Directory, если клиентские и серверные программы работают под управлением Windows 2000. Компьютеры, на которых работают клиентские и серверные программы, должны быть членами домена Windows 2000.

Чтобы объявить свое присутствие с помощью службы Active Directory, необходимо запустить серверную программу в контексте безопасности администратора домена. Если он выполняется в контексте пользователей домена, администратор домена должен изменить список управления доступом (ACL) в контейнере служб RPC. Дополнительные сведения см. в документации по Active Directory.

 

 





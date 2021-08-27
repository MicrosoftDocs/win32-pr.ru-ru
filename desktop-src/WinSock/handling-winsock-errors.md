---
description: Обработка ошибок в Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Обработка ошибок Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbb0ea47fc023ce0d6ae47f82a6bb9d732e052d5749fe58f9a405d6784d941b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097904"
---
# <a name="handling-winsock-errors"></a>Обработка ошибок Winsock

большинство функций сокетов Windows 2 не возвращают конкретную причину ошибки, когда функция возвращает значение. Некоторые функции Winsock возвращают нулевое значение в случае успеха. В противном случае \_ возвращается ошибка сокета (-1), и можно получить конкретный номер ошибки, вызвав функцию [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Для функций Winsock, возвращающих маркер, возвращаемое значение НЕДОПУСТИМого \_ сокета (0xFFFF) указывает на ошибку, и конкретный номер ошибки может быть получен путем вызова **всажетластеррор**. Для функций Winsock, возвращающих указатель, возвращаемое значение **null** указывает на ошибку, а конкретный номер ошибки можно получить, вызвав функцию **всажетластеррор** .

Код ошибки Winsock можно преобразовать в HRESULT для использования в удаленном вызове процедур (RPC) с помощью HRESULT \_ из \_ Win32. В более ранних версиях пакета средств разработки программного обеспечения (SDK) HRESULT \_ из \_ Win32 был определен как макрос в файле заголовка *Winerror. h* . в пакете Microsoft Windows Software Development Kit (SDK) значение HRESULT \_ из \_ WIN32 определяется как встроенная функция в файле заголовка *Winerror. h* .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Коды ошибок сокетов](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 




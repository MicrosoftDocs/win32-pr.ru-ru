---
title: активатеатстораже
description: Настраивает Клиент для создания экземпляров объектов на том же компьютере, что и сохраняемое состояние, которое они используют или откуда инициализируются.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- значение реестра COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8087313b8527ed95e7122d0e8dbe4fbd1ef028d7009f25937b3dc4300e9a4103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048902"
---
# <a name="activateatstorage"></a>активатеатстораже

Настраивает Клиент для создания экземпляров объектов на том же компьютере, что и сохраняемое состояние, которое они используют или откуда инициализируются.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Remarks

Это значение **reg \_ SZ** . Любое значение, которое начинается с "Y" или "y", указывает, что следует использовать **активатеатстораже** .

Функция **активатеатстораже** обеспечивает прозрачный способ, позволяющий клиентам размещать выполняющиеся объекты на том же компьютере, где находятся используемые ими данные. Это сокращает сетевой трафик, так как объект выполняет локальные вызовы файловой системы вместо вызовов по сети.

Если для **активатеатстораже** задано значение, оно становится поведением по умолчанию в вызовах функций [**кожетинстанцефромфиле**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) и [**кожетинстанцефромистораже**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) , а также в реализации моникера файла [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). Во всех этих вызовах указание структуры [**косерверинфо**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) переопределяет значение параметра **активатеатстораже** на время вызова функции. Вызывающий объект может передавать сведения о **косерверинфо** в **IMoniker:: Биндтубжект** через структуру [**привязки \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .

Значение, заданное для **активатеатстораже** , также является поведением по умолчанию при \_ указании параметра клскткс Remote Server, \_ Если на клиентском компьютере не установлены данные реестра для класса. Таким образом, клиентские приложения, написанные для использования преимуществ **активатеатстораже** , могут требовать меньше администрирования.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**клскткс**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**кожетинстанцефромфиле**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**кожетинстанцефромистораже**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**косерверинфо**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker:: Биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Регистрация серверов COM](registering-com-servers.md)
</dt> </dl>

 

 
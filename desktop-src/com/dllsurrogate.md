---
title: дллсуррогате
description: Позволяет серверам DLL выполняться в суррогатном процессе. Если указана пустая строка, используется заданный системой суррогат; в противном случае значение указывает путь к используемому суррогату.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- COM-значение реестра Дллсуррогате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413825"
---
# <a name="dllsurrogate"></a>дллсуррогате

Позволяет серверам DLL выполняться в суррогатном процессе. Если указана пустая строка, используется заданный системой суррогат; в противном случае значение указывает путь к используемому суррогату.

## <a name="registry-entry"></a>Запись реестра

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a>Комментарии

Это значение **reg \_ SZ** , указывающее, что класс является библиотекой DLL, которая должна быть активирована в суррогатном процессе, и используемый суррогатный процесс. Чтобы использовать заданный системой универсальный суррогатный процесс, задайте для *path* пустую строку или **значение NULL**. Чтобы указать другой суррогатный процесс, задайте *путь* к пути суррогата. Как и в спецификации пути к серверу в разделе [**LocalServer32**](localserver32.md) , полное указание пути не требуется. Суррогат должен быть написан для правильной связи со службой DCOM, как описано в разделе [написание пользовательского суррогата](writing-a-custom-surrogate.md).

Значение **дллсуррогате** должно присутствовать для активизации сервера DLL в суррогате. Активация относится к вызову [**кожетклассобжект**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**кокреатеинстанцеекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **кокреатеинстанцеекс**, [**Кожетинстанцефромфиле**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**кожетинстанцефромистораже**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)или [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). Выполнение библиотек DLL в суррогатном процессе предоставляет преимущества реализации исполняемого файла, включая изоляцию отказа, возможность одновременного обслуживания нескольких клиентов и предоставление серверу возможности предоставлять службы удаленным клиентам в распределенной среде.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**корегистерсуррогате**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[Суррогаты библиотеки DLL](dll-surrogates.md)
</dt> <dt>

[**дллсуррогатиксекутабле**](dllsurrogateexecutable.md)
</dt> <dt>

[**исуррогате**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 
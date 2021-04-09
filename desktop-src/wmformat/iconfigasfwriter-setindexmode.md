---
title: Иконфигасфвритер Сетиндексмоде, метод
description: Метод Сетиндексмоде позволяет приложению контролировать, будет ли файл выполняться в течение временного индексирования.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Формат Windows Media, Сетиндексмоде метод
- Сетиндексмоде метод Windows Media Format, интерфейс Иконфигасфвритер
- Интерфейс Иконфигасфвритер Windows Media Format, метод Сетиндексмоде
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070050"
---
# <a name="iconfigasfwritersetindexmode-method"></a>Метод Иконфигасфвритер:: Сетиндексмоде

Метод **сетиндексмоде** позволяет приложению контролировать, будет ли файл выполняться в течение временного индексирования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*биндексфиле* \[ окне\]
</dt> <dd>

Переменная типа **bool**; **Значение true** указывает, что файл будет временно индексироваться.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

По умолчанию [средство записи WM ASF](wm-asf-writer-filter.md) создает файлы ASF с временным индексированием. Он выполняет индексирование при остановке графа. Это поведение можно отключить, если вы хотите выполнить собственное индексирование на основе кадров в качестве этапа последующей обработки. Чтобы создать файл, индексируемый по фрейму, вызовите **сетиндексмоде**(false), создайте файл, а затем используйте методы пакета SDK Windows Media Format напрямую для создания индекса на основе фрейма для файла.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 
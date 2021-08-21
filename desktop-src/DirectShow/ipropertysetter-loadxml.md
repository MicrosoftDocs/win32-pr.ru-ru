---
description: Метод LoadXML загружает данные свойств, выраженные в язык XML (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Метод Ипропертисеттер:: LoadXML (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1779c6bcd37baad4bd423d0a46abd3741dd3a7939c1615a5871e6746729558c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952573"
---
# <a name="ipropertysetterloadxml-method"></a>Метод Ипропертисеттер:: LoadXML

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`LoadXML`Метод загружает данные свойств, выраженные в язык XML (XML).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PXML* \[ окне\]
</dt> <dd>

Указатель на интерфейс **IUnknown** элемента XML, созданного средством синтаксического анализа Microsoft XML.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                                  | Описание                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | Нет данных свойства.<br/>    |
| <dl> <dt>**\_ОК**</dt> </dl>                         | Успешно.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                | Недостаточно памяти.<br/> |
| <dl> <dt>**\_ \_ Недопустимый \_ Формат файла VFW E \_**</dt> </dl> | Недопустимый формат.<br/>      |



 

## <a name="remarks"></a>Remarks

Как правило, приложениям не требуется использовать этот метод. Алгоритм DES использует его для внутренней загрузки свойств из файлов КСТЛ.

Чтобы использовать этот метод, создайте объект **IXMLDocument** и используйте его для синтаксического анализа XML-файла. Затем используйте объект **IXMLDocument** для получения объектов **иксмлелемент** . Если у объекта есть свойства, можно передать указатель **иксмлелемент** в метод **LoadXml** . Метод загружает свойства в метод задания свойства.

> [!Note]  
> интерфейсы **IXMLDocument** и **иксмлелемент** реализуются в MSXML (MSXML) версии 1,0, но не реализованы в более поздних версиях MSXML.

 

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипропертисеттер**](ipropertysetter.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 





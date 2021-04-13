---
description: Удаляет пакет исключения.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: Функция Унинсталлкомпонент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647934"
---
# <a name="uninstallcomponent-function"></a>Функция Унинсталлкомпонент

Удаляет пакет исключения.

## <a name="syntax"></a>Синтаксис


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Компгуид* \[ в необязательное\]
</dt> <dd>

Идентификатор GUID удаляемого компонента исключения.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Флаги, используемые для управления поведением при установке. Этот параметр может быть сочетанием следующих значений.



| Значение                                                                                                                                                                                                         | Значение                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <dt>**\_NOUI) флаги Comp \_**</dt> </dl>                                          | Подавляет весь пользовательский интерфейс.<br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <dt>**\_Флаги Comp \_ обновления \_ DLLCACHE**</dt> </dl>        | Принудительное обновление каталога DLLCACHE при обновлении системного файла.<br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <dt>**\_Флаги \_ comp \_ используют \_ кэш SVCPACK**</dt> </dl> | Использует файлы, кэшированные при установке пакета обновления Windows, для замены резервных копий файлов.<br/> |



 

</dd> <dt>

*Вермажор* \[ в необязательное\]
</dt> <dd>

Основная версия компонента исключения, который необходимо удалить.

</dd> <dt>

*Верминор* \[ в необязательное\]
</dt> <dd>

Дополнительный номер версии компонента исключения, который необходимо удалить.

</dd> <dt>

*Вербуилд* \[ в необязательное\]
</dt> <dd>

Версия сборки компонента исключения, который необходимо удалить.

</dd> <dt>

*Веркфе* \[ в необязательное\]
</dt> <dd>

Редакция исправления компонента исключения, который необходимо удалить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Пакеты исключений — это системные файлы Windows, выпущенные за пределами полной версии пакета Windows и обновленными файлами операционной системы. Пакеты исключений разрабатываются только командами операционной системы, которым была предоставлена авторизация на обновление системных файлов Windows.

Для установки и удаления файлов, не защищенных с помощью защиты файлов Windows, используйте функции, описанные в статье [Общие функции установки](https://msdn.microsoft.com/library/ms794585.aspx). Чтобы установить драйверы устройств, поставщиков следует использовать функции, описанные в статье [функции установки устройств](https://msdn.microsoft.com/library/ms792954.aspx) и [функции PnP Configuration Manager](https://msdn.microsoft.com/library/ms790838.aspx).

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msoobci.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>


</dt> <dt>

[**инсталлкомпонентв**](installcomponentw.md)
</dt> </dl>

 

 

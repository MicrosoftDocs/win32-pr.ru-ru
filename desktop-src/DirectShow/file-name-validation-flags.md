---
description: Эти флаги определяют поведение указателя мультимедиа.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Флаги проверки имени файла (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 44bbeebc344edf1c6a9c5a5d287bea7cdfe87e96d9af09a65417411d6cd43820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015772"
---
# <a name="file-name-validation-flags"></a>Флаги проверки имени файла

\[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

Эти флаги определяют поведение указателя мультимедиа.



| Константа/значение                                                                                                                                                                                                                                               | Описание                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**СФН \_ ВАЛИДАТЕФ \_ Проверка**</dt> <dt>0x01</dt> </dl>                   | Проверьте правильность имен файлов. Этот флаг необходимо установить для проверки имен файлов. В противном случае другие флаги не оказывают никакого влияния.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**СФН \_ \_Всплывающее меню валидатеф**</dt> <dt>0x02</dt> </dl>                   | Если файл не найден, отобразите диалоговое окно Открытие файла для конечного пользователя.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**СФН \_ ВАЛИДАТЕФ \_ теллме**</dt> <dt>0x04</dt> </dl>                | Если отсутствующий файл найден, ненадолго отобразите окно сообщения с именем и расположением файла. Этот флаг в основном полезен в целях тестирования. возможно, окно сообщения не подходит для розничного продукта.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**СФН \_ ВАЛИДАТЕФ \_ заменить**</dt> <dt>0x08</dt> </dl>             | Если отсутствующий файл найден, обновите имя исходного объекта. (Допускается только в методе [**иамтимелине:: валидатесаурценамес**](iamtimeline-validatesourcenames.md) .)<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**СФН \_ ВАЛИДАТЕФ \_ уселокал**</dt> <dt>0x10</dt> </dl>          | Всегда используйте локальный файл, даже если версия файла существует в сети.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**СФН \_ ВАЛИДАТЕФ \_**</dt> , отличный от Find <dt>0x20</dt> </dl>                | Не искать отсутствующие файлы. Имена файлов по-прежнему проверяются, если \_ установлен \_ флаг проверки СФН валидатеф.<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**СФН \_ ВАЛИДАТЕФ \_ игноремутед**</dt> <dt>0x40</dt> </dl> | Не учитывать отключенные исходные объекты. (Допускается только в методе [**иамтимелине:: валидатесаурценамес**](iamtimeline-validatesourcenames.md) .)<br/>                                                                                |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Кедит. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Имедиалокатор:: Финдмедиафиле**](imedialocator-findmediafile.md)
</dt> <dt>

[**Ирендеренгине:: Сетсаурценамевалидатион**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 





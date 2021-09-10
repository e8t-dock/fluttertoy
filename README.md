## Flutter Toy

    ListView.builder(
      itemCount: users.length,
      padding: const EdgeInsets.only(top: 16),
      physics: const NeverScrollableScrollPhysics(),
      itemBuilder: (context, index) {
        final user = users[index];
        return ChatWidget(
            name: user.name,
            messageText: user.messageText,
            imageURL: user.imageURL,
            time: user.time,
            isRead: (index == 0 || index == 3 ? true : false));
      }
    )
